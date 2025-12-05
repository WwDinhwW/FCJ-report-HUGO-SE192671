---
title: "7. Khởi tạo EC2 Instances"
type: "page"
weight: 7
---

Bây giờ bạn sẽ triển khai hai EC2 instances:

| Instance    | Subnet         | Truy cập                                               |
|-------------|----------------|--------------------------------------------------------|
| EC2-Public  | Public-Subnet  | SSH trực tiếp từ Internet                              |
| EC2-Private | Private-Subnet | Không có Public IP — chỉ truy cập thông qua EC2-Public |

Cả hai instance sẽ sử dụng cùng một AMI và cùng loại instance để đơn giản hóa cấu hình.

---

### 7.1 Tạo Key Pair

1. Mở **EC2 Console**
2. Ở mục điều hướng bên trái → chọn **Key Pairs**
3. Nhấn **Create key pair**
4. Cấu hình:
    - **Name:** `Workshop-Key`
    - **Type:** RSA
    - **Format:** `.pem` (Linux/Mac) hoặc `.ppk` (Windows PuTTY)
5. Tải xuống và lưu trữ an toàn

![Key Pair Creation Menu](/images/5-Workshop/7-EC2/ec2-keypair-creation.png)

> _Key này sẽ được sử dụng cho SSH._

---

### 7.2 Tạo EC2 Instance ở Public Subnet

1. Trong EC2 Console → chọn **Instances** → nhấn **Launch instances**
2. Name: `EC2-Public`
3. Chọn AMI:
    - **Amazon Linux**
4. Instance type: **t3.micro** (Hỗ trợ Free Tier)
5. Chọn key pair: `Workshop-Key`
6. Network settings (nhấn **Edit** để mở menu):
    - **VPC:** Workshop-VPC
    - **Subnet:** Public-Subnet
    - **Auto-assign Public IP:** Enabled
7. Cấu hình Security Group:
    - Tạo mới tên: `Public-EC2-SG`
    - Inbound Rule:
        - Type: **SSH**
        - Source Type: `Custom`
        - Source: `0.0.0.0/0`
8. Giữ nguyên các thiết lập còn lại
9. Nhấn **Launch instance**

![EC2 Instance Launch Menu](/images/5-Workshop/7-EC2/ec2-instance-creation.png)

---

### 7.3 Tạo EC2 Instance ở Private Subnet

1. Trong EC2 Console → **Instances** → nhấn **Launch instances** một lần nữa
2. Name: `EC2-Private`
3. AMI + loại instance = giống với Public EC2
4. Chọn key pair: `Workshop-Key`
5. Network settings:
    - **VPC:** Workshop-VPC
    - **Subnet:** Private-Subnet
    - **Auto-assign Public IP:** Disabled
6. Security Group:
    - Tên: `Private-EC2-SG`
    - Type: **SSH**
    - Source Type: `Custom`
    - Source: `Public-EC2-SG` **(không phải Internet)**

📸 _Screenshot phần này: cấu hình EC2 Private không có Public IP_

![EC2 Private Instance Launch Menu](/images/5-Workshop/7-EC2/ec2-instance-private-creation.png)

---

### 7.4 Kiểm tra Instances

| Instance    | IP                 | Kết quả mong đợi                       |
|-------------|--------------------|----------------------------------------|
| EC2-Public  | Có IPv4 Public     | Có thể SSH từ máy cá nhân              |
| EC2-Private | Không có Public IP | Chỉ truy cập được thông qua EC2-Public |

![EC2 Instances List](/images/5-Workshop/7-EC2/ec2-instance-list.png)