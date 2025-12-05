---
title: "2. Yêu cầu trước khi thực hiện"
type: "page"
weight: 2
---

Trước khi bắt đầu workshop, hãy bảo đảm rằng bạn có đủ các điều kiện sau:

### Tài khoản & Quyền truy cập

- Một **AWS Account**
- **IAM User** với quyền truy cập vào:
    - Amazon VPC
    - Amazon EC2
    - Elastic IP
    - NAT Gateway
    - Internet Gateway
- Khuyến nghị sử dụng policy: **AdministratorAccess** (chỉ dành cho mục đích thực hành)

> Nếu bạn đang sử dụng IAM User, hãy đảm bảo rằng bạn có Access Key hoặc thông tin đăng nhập AWS Console.

### Lưu ý chi phí

Workshop này có bao gồm việc tạo **NAT Gateway**, đây là dịch vụ tính phí.
Để giảm thiểu chi phí, hãy xóa toàn bộ tài nguyên sau khi hoàn thành phần Cleanup.

_chi phí dự kiến: ~ vài USD nếu tài nguyên được xóa trong ngày_

### Công cụ cần thiết

| Công cụ                       | Mục đích sử dụng                                           |
|-------------------------------|------------------------------------------------------------|
| AWS Management Console        | Giao diện chính để tạo VPC, Subnet và Route Table          |
| SSH client (PuTTY / Terminal) | Dùng để kết nối SSH vào EC2 instances                      |
| Key Pair                      | Cần thiết để đăng nhập EC2 (bạn sẽ tạo trong workshop này) |

### Lựa chọn Region

Khuyến nghị sử dụng Region gần bạn nhất để có độ trễ thấp.  
Ví dụ: **ap-southeast-1 (Singapore)** cho người dùng tại Việt Nam.

> Bạn phải sử dụng cùng một Region cho tất cả các bước trong workshop.