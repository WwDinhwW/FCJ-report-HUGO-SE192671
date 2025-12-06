---
title: "Tuần 12: Củng cố kiến trúc bảo mật AWS và hoàn thiện kỹ năng bảo vệ hệ thống đám mây"
type: "page"
weight: "12"
---

# Mục tiêu:
* Hiểu sâu về **Security Pillar** trong AWS Well-Architected Framework và các chiến lược bảo mật hiện đại.
* Nắm vững quản trị danh tính, cơ chế phát hiện, bảo vệ hạ tầng và bảo mật dữ liệu trên AWS.
* Tăng cường kỹ năng triển khai bảo mật thực tế: IAM, KMS, logging, phân tách mạng, bảo vệ workload.
* Tổng hợp toàn bộ kiến thức bảo mật để hoàn thiện nội dung cuối cùng cho Report Site.

# Các công việc hoàn thành:
| Thứ | Công việc                                                                                                                                                                                                                                                                                          | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu              |
|-----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|-----------------|-----------------------------|
| 2   | - Học các nguyên tắc cốt lõi của **Security Pillar**: Least Privilege, Zero Trust, Defense in Depth. <br> - Ôn lại **Shared Responsibility Model** và cách áp dụng vào từng loại workload trên AWS.                                                                                                | 24/11/2025   | 24/11/2025      | AWS Docs, Internet          |
| 3   | - Tìm hiểu best practices về quản trị truy cập: IAM Roles, Policies, MFA, credential rotation, Access Analyzer. <br> - Nghiên cứu **IAM Identity Center** và quản lý permission boundaries cho môi trường nhiều tài khoản (multi-account).                                                         | 25/11/2025   | 25/11/2025      | AWS Docs, tài liệu bảo mật  |
| 4   | - Học về cơ chế **Detection & Monitoring**: CloudTrail, GuardDuty, Security Hub. <br> - Phân tích kiến trúc logging theo nhiều lớp: VPC Flow Logs, ALB Logs, S3 Access Logs, và routing alert qua EventBridge.                                                                                     | 26/11/2025   | 26/11/2025      | AWS Security Docs, Internet |
| 5   | - Tập trung vào **Infrastructure Protection**: phân tách mạng VPC, thiết kế subnet private/public, Security Group vs NACLs, tích hợp WAF và Shield. <br> - Ôn tập các cơ chế bảo vệ workload (EC2, ECS/EKS).                                                                                       | 27/11/2025   | 27/11/2025      | AWS Docs, tài nguyên nội bộ |
| 6   | - Học về **Data Protection**: mã hóa dữ liệu (at-rest & in-transit), chính sách KMS, key rotation, Secrets Manager và Parameter Store. <br> - Tổng hợp các playbook **Incident Response**: lộ IAM key, S3 public exposure, phát hiện malware, cô lập workload và tự động hóa phản ứng bằng Lambda. | 28/11/2025   | 28/11/2025      | AWS IR Docs, Security Blogs |

# Kết quả đạt được:
* Nắm vững toàn bộ Security Pillar và áp dụng được các mô hình Least Privilege và Zero Trust.
* Tăng cường kỹ năng quản trị danh tính, phân quyền và quản lý truy cập trong môi trường nhiều tài khoản.
* Hiểu rõ hệ thống phát hiện và giám sát (CloudTrail, GuardDuty, Security Hub) và kiến trúc logging theo nhiều tầng.
* Thành thạo các kỹ thuật bảo vệ hạ tầng: segmentation, WAF, Shield, thiết kế SG/NACL hợp lý.
* Nắm chắc nền tảng bảo mật dữ liệu với KMS, mã hóa và quản lý secrets.