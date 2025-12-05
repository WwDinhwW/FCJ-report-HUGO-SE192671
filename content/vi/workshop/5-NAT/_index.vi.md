---
title: "5. Tạo NAT Gateway"
type: "page"
weight: 5
---

NAT Gateway cho phép các instance trong **Private Subnet** truy cập Internet
_mà không bị lộ trực tiếp ra bên ngoài_. Nhờ đó, EC2 trong private subnet có thể `yum install`, tải bản cập nhật, v.v.

### 5.1 Cấp phát Elastic IP

1. Trong bảng điều hướng của VPC, chọn **Elastic IPs**
2. Nhấn **Allocate Elastic IP address**
3. Giữ nguyên cấu hình mặc định
4. Nhấn **Allocate**

![Allocate Elastic IP window](/images/5-Workshop/5-NAT/elastic-IP-allocate.png)

---

### 5.2 Tạo NAT Gateway

1. Trong bảng điều hướng VPC, mở **NAT gateways**
2. Nhấn **Create NAT gateway**
3. Cấu hình như sau:

| Trường                | Giá trị                 |
|-----------------------|-------------------------|
| Name                  | `Workshop-NAT`          |
| Availability mode     | Zonal                   |
| Subnet                | `Public-Subnet`         |
| Connectivity type     | Public                  |
| Elastic IP allocation | Chọn Elastic IP vừa tạo |

4. Nhấn **Create NAT gateway**

![Create NAT Gateway screen with selected subnet + EIP](/images/5-Workshop/5-NAT/NAT-creation.png)

---

### 5.3 Chờ NAT Gateway chuyển sang trạng thái "Available"

- Trạng thái ban đầu: **Pending**
- Chờ đến khi chuyển thành **Available**

![NAT Gateway state](/images/5-Workshop/5-NAT/NAT-state.png)

---

### Kiểm tra kết quả

| Resource                     | Trạng thái |
|------------------------------|------------|
| NAT Gateway (`Workshop-NAT`) | Available  |
| Elastic IP                   | Associated |

Bạn đã sẵn sàng cấu hình tuyến truy cập Internet cho Private Subnet thông qua NAT.