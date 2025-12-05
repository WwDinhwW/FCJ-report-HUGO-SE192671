---
title: "4. Tạo Internet Gateway"
type: "page"
weight: 4 
---

Internet Gateway (IGW) cho phép các tài nguyên trong **Public Subnet** gửi và nhận lưu lượng từ Internet.
Nếu không có IGW, ngay cả khi subnet có Public IP thì vẫn sẽ bị cô lập khỏi Internet.

### 4.1 Tạo một Internet Gateway

1. Trong AWS Console, mở dịch vụ **VPC**
2. Ở bảng điều hướng bên trái, chọn **Internet Gateways**
3. Nhấn **Create internet gateway**
4. Nhập giá trị:
    - **Name tag:** `Workshop-IGW`
5. Nhấn **Create internet gateway**

![Internet Gateway Creation Menu](/images/5-Workshop/4-IG/IG-creation.png)

---

### 4.2 Gắn Internet Gateway vào VPC

1. Sau khi IGW được tạo, chọn **Actions → Attach to VPC**
2. Chọn **Workshop-VPC**
3. Nhấn **Attach internet gateway**

![Internet Gateway Attach Menu](/images/5-Workshop/4-IG/IG-attach-vpc.png)

---

### Kiểm tra kết quả

Bạn sẽ thấy kết quả như sau:

| Resource     | Status                   |
|--------------|--------------------------|
| Workshop-IGW | Attached to Workshop-VPC |

![Internet Gateway List](/images/5-Workshop/4-IG/IG-list.png)