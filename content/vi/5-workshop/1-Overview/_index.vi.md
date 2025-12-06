---
title: "1. Tổng quan"
type: "page"
weight: 1
---

# Xây dựng AWS VPC cơ bản với Public & Private Subnets

Trong workshop này, bạn sẽ xây dựng một nền tảng mạng đơn giản trên AWS bằng **Amazon VPC (Virtual Private Cloud)**.
Mục tiêu là giúp người mới bắt đầu hiểu cách hoạt động của mạng trong môi trường điện toán đám mây, cũng như cách các
thành phần khác nhau kết nối với nhau để tạo thành một hệ thống an toàn và có kiểm soát.

Bạn sẽ tạo một VPC với hai subnet:

+ **Public Subnet** – cho phép tài nguyên (như EC2 instances) truy cập Internet trực tiếp.
+ **Private Subnet** – cách ly với Internet công khai theo mặc định để đảm bảo bảo mật tốt hơn.

Để cho phép private subnet có thể tải gói, cập nhật và sử dụng dịch vụ trực tuyến mà không bị lộ ra Internet công khai,
bạn sẽ cấu hình:

+ **Internet Gateway (IGW)** – cho phép lưu lượng mạng từ Public Subnet đi/đến Internet.
+ **NAT Gateway** – cho phép các instance trong Private Subnet truy cập Internet *gián tiếp* mà không cần gán Public IP.

Kết thúc workshop, bạn sẽ tạo hai EC2 instance — mỗi instance nằm trong một subnet — và kiểm tra khả năng kết nối giữa
chúng, đồng thời quan sát vai trò của định tuyến và gateway.

Workshop thực hành này hướng dẫn bạn tiếp cận các kiến thức nền tảng về AWS Networking thông qua các bước thao tác trực
tiếp trên Console.
Phù hợp cho người mới muốn xây dựng sự tự tin khi làm việc với VPC.