---
title: "Tuần 11: Tối ưu phân phối nội dung tại Edge và tăng cường bảo mật ứng dụng Web trên AWS"
type: "page"
weight: "11"
---

# Mục tiêu:
* Nắm vững kiến trúc **Edge Services** và cơ chế phân phối nội dung toàn cầu của AWS.
* Tối ưu hiệu năng và độ trễ thấp cho ứng dụng thông qua CloudFront.
* Hiểu các kỹ thuật bảo mật ứng dụng Web: lọc request, giảm thiểu tấn công, bảo vệ trước bot và các lỗ hổng OWASP.
* Tích hợp kiến thức hiệu năng và bảo mật vào backend dự án và trang Report Site.

# Các công việc hoàn thành:
| Thứ | Công việc                                                                                                                                                                                                              | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu            |
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|-----------------|---------------------------|
| 2   | - Tìm hiểu hệ thống **Content Delivery Network (CDN)** của AWS và kiến trúc Edge toàn cầu. <br> - Học cách CloudFront giảm độ trễ thông qua caching, routing, và tối ưu vị trí phân phối.                              | 17/11/2025   | 17/11/2025      | AWS Docs, Internet        |
| 3   | - Nghiên cứu các kỹ thuật tối ưu CloudFront nâng cao: cache policy, điều chỉnh TTL, origin failover, và kiểm soát bảo mật tại Edge. <br> - Ghi chép và bổ sung tài liệu vào phần “Cloud Optimization” của Report Site. | 18/11/2025   | 18/11/2025      | AWS Docs, tài liệu nội bộ |
| 4   | - Học về **AWS WAF**: cơ chế lọc request, chặn traffic độc hại, giảm thiểu các mối đe doạ như SQLi/XSS. <br> - Phân tích bộ **OWASP Top 10** và cách các bộ rule của WAF giúp phòng chống các lỗ hổng phổ biến.        | 19/11/2025   | 19/11/2025      | AWS Docs, Security Blogs  |
| 5   | - Tìm hiểu kỹ thuật **bot mitigation**, phát hiện bất thường và giới hạn tần suất (rate-limiting) để bảo vệ workload quy mô lớn. <br> - Khám phá tích hợp bảo mật theo từng lớp giữa CloudFront, WAF và Shield.        | 20/11/2025   | 20/11/2025      | AWS Docs, Internet        |
| 6   | - Thực hành áp dụng kiến thức hiệu năng và bảo mật vào backend dự án. <br> - Cập nhật tài liệu nội bộ: tối ưu CloudFront, thiết kế rule WAF, và mô hình triển khai bảo mật cho ứng dụng Web.                           | 21/11/2025   | 21/11/2025      | Internet, tài liệu nội bộ |

# Kết quả đạt được:
* Hiểu sâu về kiến trúc Edge và quy trình phân phối nội dung trên AWS.
* Thành thạo các kỹ thuật tối ưu CloudFront cho hiệu năng cao, độ trễ thấp và chi phí hợp lý.
* Nắm vững kiến thức bảo mật ứng dụng Web: WAF, giảm thiểu tấn công, và OWASP Top 10.
* Biết cách phát hiện và chống bot, tự động hoá bảo vệ ứng dụng ở quy mô lớn.