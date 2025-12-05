---
title: "8. Kiểm tra kết nối"
type: "page"
weight: 8
---

Bây giờ cả hai EC2 instances đã chạy, đây là lúc kiểm tra hành vi mạng và xác nhận rằng VPC đang hoạt động đúng.
Phần này kiểm tra ba yếu tố:

1. EC2-Public có thể SSH từ máy cá nhân
2. EC2-Private chỉ có thể truy cập thông qua EC2-Public (không trực tiếp từ Internet)
3. EC2-Private có thể truy cập Internet thông qua NAT Gateway

---

### 8.1 Kết nối vào Public EC2 Instance

1. Mở **EC2 Console** → **Instances**
2. Sao chép địa chỉ **Public IPv4** của **EC2-Public**
3. SSH vào instance

> Bước này phụ thuộc vào hệ điều hành và công cụ bạn sử dụng.  
> Trong workshop này, chúng tôi sử dụng PowerShell trên Windows 11.  
> Bạn có thể dùng công cụ khác nếu muốn.

```bash
ssh -i "Workshop-Key.pem" ec2-user@<PUBLIC_IP_HERE>
```

> Ví dụ: ssh -i "Workshop-Key.pem" ec2-user@54.218.10.102

4. Sau khi chạy lệnh, màn hình sẽ hiển thị tương tự sau:

![SSH into public EC2 instance](/images/5-Workshop/8-Connectivity-Tests/ssh-into-public-from-powershell.png)

> Đã kết nối vào EC2-Public. Một số thông tin đã được làm mờ vì lý do bảo mật.

---

### 8.2 SSH từ EC2-Public vào EC2-Private

1. Trước khi thực hiện, bạn cần sao chép key pair vào instance **EC2-Public**

> Việc đặt key truy cập lên EC2 không phải phương án AWS khuyến nghị  
> vì có thể gây rủi ro bảo mật.  
> Tuy nhiên, để phục vụ mục đích kiểm thử trong workshop, bạn có thể thực hiện.

2. Từ terminal máy cá nhân (không trong phiên SSH nào), chạy lệnh:

```bash
scp -i "Workshop-Key.pem" Workshop-Key.pem ec2-user<PUBLIC_IP_HERE>:/home/ec2-user/
```

> Lệnh này sao chép key vào EC2-Public để dùng SSH truy cập EC2-Private sau đó.

3. Tiếp theo SSH vào **EC2-Public** (như bước 8.1) và chạy lệnh:

```bash
chmod 400 Workshop-Key.pem
```

> Lệnh này giới hạn quyền truy cập file key, đảm bảo có thể dùng để SSH vào EC2-Private.

4. Sau đó chạy lệnh:

```bash
ssh -i "Workshop-Key.pem" ec2-user@<PRIVATE_IP_HERE>
```

![SSH into private instance from public instance](/images/5-Workshop/8-Connectivity-Tests/ssh-into-private-from-public.png)

> Thành công — bạn đã SSH vào EC2-Private từ EC2-Public, đúng với mô hình bảo mật đã cấu hình.

---

### 8.3 Kiểm tra khả năng truy cập Internet từ EC2-Private

1. Chạy các lệnh:

```bash
ping -c 3 google.com
sudo yum update -y
```

2. Kết quả mong đợi:

| Hành động       | Kết quả                 |
|-----------------|-------------------------|
| ping google.com | Trả về phản hồi (Reply) |
| yum update      | Tải gói thành công      |

→ Nếu đúng, NAT Gateway hoạt động như mong đợi.

![Test internet connection of private instance](/images/5-Workshop/8-Connectivity-Tests/ssh-private-test-internet.png)

> EC2-Private đã truy cập Internet thành công thông qua NAT Gateway.

---

### 8.4 Xác minh hành vi bảo mật (Kiểm tra quan trọng)

| Kiểm tra                         | Kết quả mong đợi  |
|----------------------------------|-------------------|
| Máy bạn → SSH vào EC2-Private    | Bị chặn           |
| EC2-Public → SSH vào EC2-Private | Được phép         |
| EC2-Private → Internet           | Hoạt động via NAT |

→ Điều này chứng minh rằng cơ chế public được kiểm soát, private vẫn an toàn nhưng vẫn có Internet khi cần.

![SSH into private instance from local machine](/images/5-Workshop/8-Connectivity-Tests/ssh-into-private-from-pc.png)

> Đúng như mong đợi — kết nối từ máy cá nhân đến EC2-Private bị từ chối.  
> Cơ chế bảo mật hoạt động chính xác.

---

### Hoàn thành kiểm tra kết nối