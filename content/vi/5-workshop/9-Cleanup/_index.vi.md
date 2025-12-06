---
title: "9. Dọn dẹp tài nguyên"
type: "page"
weight: 9
---

Để tránh phát sinh chi phí không cần thiết — đặc biệt là từ **NAT Gateway** — bạn nên xóa toàn bộ tài nguyên sau khi
hoàn thành workshop.

Thực hiện theo các bước sau theo đúng thứ tự:

---

### 9.1 Terminate EC2 Instances

1. Mở **EC2 Console**
2. Chọn cả `EC2-Public` và `EC2-Private`
3. Nhấn **Instance state → Terminate** (quá trình có thể mất vài phút)
4. Xác nhận hành động

![EC2 instances termination](/images/5-Workshop/9-Cleanup/ec2-instance-termination.png)

---

### 9.2 Xóa NAT Gateway

1. Truy cập **VPC Console → NAT Gateways**
2. Chọn `Workshop-NAT`
3. Nhấn **Actions → Delete NAT Gateway** (chờ trong giây lát)
4. Xác nhận xóa

> Chờ đến khi NAT Gateway chuyển trạng thái **Deleted** trước khi tiếp tục bước tiếp theo.

![EC2 instances termination](/images/5-Workshop/9-Cleanup/NAT-termination.png)

---

### 9.3 Giải phóng Elastic IP

Sau khi NAT Gateway bị xóa:

1. Đi tới **Elastic IPs**
2. Chọn địa chỉ đã cấp phát
3. Nhấn **Actions → Release Elastic IP address**
4. Xác nhận (danh sách Elastic IP trống)

---

### 9.4 Gỡ và xóa Internet Gateway

1. Mở **Internet Gateways**
2. Chọn `Workshop-IGW`
3. Nhấn **Actions → Detach from VPC**
4. Sau đó **Actions → Delete Internet gateway**
5. Xác nhận xóa (danh sách Internet Gateways trống)

---

### 9.5 Xóa Subnets

1. Truy cập **Subnets**
2. Xóa `Public-Subnet`
3. Xóa `Private-Subnet`
4. Xác nhận xóa (danh sách Subnets trống)

---

### 9.6 Xóa VPC

1. Mở **VPC Console**
2. Chọn `Workshop-VPC`
3. Nhấn **Actions → Delete VPC**
4. Xác nhận xóa (danh sách VPC trống)

---

### 9.7 Xóa Route Tables

1. Mở **Route Tables**
2. Chọn `Public-RT` → **Delete**
3. Chọn `Private-RT` → **Delete**
4. Xác nhận xóa (route tables đã tạo không còn tồn tại)

---

### Dọn dẹp hoàn tất