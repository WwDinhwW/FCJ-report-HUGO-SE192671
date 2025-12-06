---
title: "3. Tạo VPC & Subnet"
type: "page"
weight: 3
---

Trong phần này, bạn sẽ tạo Virtual Private Cloud (VPC) của riêng mình và thiết lập hai subnet:

- 1 Public Subnet (có thể truy cập Internet)
- 1 Private Subnet (không truy cập Internet trực tiếp)

### 3.1 Tạo VPC

1. Mở **AWS Management Console**
2. Điều hướng đến **Services → VPC**
3. Chọn **Create VPC**
4. Chọn tùy chọn **VPC Only**
5. Nhập thông tin:
    - **Name tag:** `Workshop-VPC`
    - **IPv4 CIDR:** `10.0.0.0/16`
6. Giữ các thiết lập khác ở mặc định
7. Nhấn **Create VPC**

![VPC Creation Menu](/images/5-Workshop/3-VPC-Subnets/vpc-creation.png)

---

### 3.2 Tạo Public Subnet

1. Trong menu bên trái, chọn **Subnets**
2. Nhấn **Create subnet**
3. Cấu hình như sau:
    - **VPC:** `Workshop-VPC`
    - **Subnet name:** `Public-Subnet`
    - **Availability Zone:** (tùy chọn, ví dụ: `ap-southeast-1a`)
    - **IPv4 CIDR block:** `10.0.1.0/24`
4. Nhấn **Create subnet**

![Subnet Creation Menu](/images/5-Workshop/3-VPC-Subnets/public-subnet-creation.png)

---

### 3.3 Tạo Private Subnet

1. Nhấn **Create subnet** một lần nữa
2. Nhập thông tin:
    - **VPC:** `Workshop-VPC`
    - **Subnet name:** `Private-Subnet`
    - **Availability Zone:** (có thể giống hoặc khác Public Subnet)
    - **IPv4 CIDR block:** `10.0.2.0/24`
3. Nhấn **Create subnet**

> Quy trình tương tự như bước 3.2, chỉ khác một số giá trị. Vui lòng tham khảo 3.2 để đối chiếu.

---

### 3.4 Bật Auto-Assign Public IP (chỉ cho Public Subnet)

1. Truy cập mục **Subnets**
2. Chọn **Public-Subnet**
3. Nhấn **Actions → Edit subnet settings**
4. Bật tùy chọn:
    - ☑ **Auto-assign public IPv4**
5. Nhấn **Save**

![Subnet Setting Menu](/images/5-Workshop/3-VPC-Subnets/public-subnet-IP-assign.png)

---

**Kết quả mong đợi:**
Bạn đã tạo thành công một VPC với hai subnet sẵn sàng sử dụng.

Các thành phần đã được tạo:

| Resource           | Name           | CIDR        |
|--------------------|----------------|-------------|
| VPC                | Workshop-VPC   | 10.0.0.0/16 |
| Subnet 1 (Public)  | Public-Subnet  | 10.0.1.0/24 |
| Subnet 2 (Private) | Private-Subnet | 10.0.2.0/24 |