---
title: "6. Cấu hình Route Table"
type: "page"
weight: 6
---

Route Tables quyết định hướng lưu lượng mạng bên trong VPC của bạn.
Trong phần này, bạn sẽ:

- Tạo route table riêng cho public subnet và private subnet
- Định tuyến lưu lượng Internet từ public subnet → Internet Gateway
- Định tuyến lưu lượng từ private subnet → NAT Gateway để truy cập Internet đầu ra

---

### 6.1 Tạo Route Table cho Public Subnet

1. Trong VPC Console, mở **Route Tables**
2. Nhấn **Create route table**
3. Nhập:
    - **Name:** `Public-RT`
    - **VPC:** `Workshop-VPC`
4. Nhấn **Create route table**

![Route Table Creation Menu](/images/5-Workshop/6-RouteTB/RT-creation.png)

---

### 6.2 Thêm tuyến đến Internet Gateway

1. Chọn route table **Public-RT**
2. Chuyển đến tab **Routes**
3. Nhấn **Edit routes → Add route**
4. Nhập:
    - **Destination:** `0.0.0.0/0`
    - **Target:** `Internet Gateway (Workshop-IGW)`
5. Nhấn **Save changes**

![Route Table add new route](/images/5-Workshop/6-RouteTB/RT-add-route.png)

---

### 6.3 Gán Public Subnet vào Public Route Table

1. Vẫn tại giao diện của Public-RT
2. Chọn **Subnet associations**
3. Trong tab **Explicit subnet associations** → chọn **Edit subnet associations**
4. Tick chọn **Public-Subnet**
5. Nhấn **Save**

![Route Table add Public Subnet](/images/5-Workshop/6-RouteTB/RT-add-subnet.png)

---

### 6.4 Tạo Route Table cho Private Subnet

1. Nhấn **Create route table**
2. Nhập:
    - **Name:** `Private-RT`
    - **VPC:** `Workshop-VPC`
3. Nhấn **Create route table**

> Quy trình tương tự bước 6.1, chỉ thay đổi tên và subnet liên quan.

---

### 6.5 Thêm tuyến đến NAT Gateway (cho Private Subnet)

1. Chọn **Private-RT**
2. Chuyển đến **Routes → Edit routes**
3. Thêm:
    - **Destination:** `0.0.0.0/0`
    - **Target:** `NAT Gateway (Workshop-NAT)`
4. Nhấn **Save**

![Route Table add new route to NAT Gateway](/images/5-Workshop/6-RouteTB/RT-add-route-NAT.png)

---

### 6.6 Gán Private Subnet

1. Tại route table **Private-RT**, chuyển sang **Subnet associations**
2. Trong tab **Explicit subnet associations** → chọn **Edit subnet associations**
3. Tick chọn **Private-Subnet**
4. Nhấn **Save**

![Route Table add Private Subnet](/images/5-Workshop/6-RouteTB/RT-add-subnet-private.png)

---

### Kiểm tra kết quả

Bạn sẽ thấy kết nối định tuyến như sau:

| Route Table | Subnet         | Tuyến Internet   |
|-------------|----------------|------------------|
| Public-RT   | Public-Subnet  | Internet Gateway |
| Private-RT  | Private-Subnet | NAT Gateway      |

Tại thời điểm này, cấu trúc mạng VPC đã được thiết lập và hoạt động đầy đủ.
Tiếp theo — chúng ta triển khai EC2 instance để kiểm tra khả năng kết nối.