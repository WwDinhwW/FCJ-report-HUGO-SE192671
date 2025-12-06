---
title: "Sự kiện 4"
type: "page"
---

# BÀI THU HOẠCH SỰ KIỆN: "AWS Edge Services Workshop"

**Ngày:** Thứ Tư, 19 tháng 11, 2025.

**Thời gian:** 8:30 AM – 5:00 PM

**Địa điểm:** Văn phòng AWS Vietnam, Tòa nhà Bitexco Financial Tower, Quận 1, TP.HCM.

**Mục tiêu sự kiện:** Nâng cao kiến thức về phân phối nội dung toàn cầu với CloudFront, bảo vệ ứng dụng web bằng
AWS WAF, và thực hành triển khai tối ưu hóa & bảo mật ứng dụng qua các phiên Hands-on trực tiếp.

## TÓM TẮT CHƯƠNG TRÌNH

| Thời gian         | Chủ đề                                                   | Diễn giả                                       | Trọng tâm Chính                                                                       |
|:------------------|:---------------------------------------------------------|:-----------------------------------------------|:--------------------------------------------------------------------------------------|
| **08:00 – 08:30** | Registration & Networking                                | —                                              | Giao lưu, check-in, làm quen với các kiến trúc sư AWS.                                |
| **08:30 – 09:30** | From Edge to Origin: CloudFront as Your Foundation       | Nguyễn Gia Hưng – Head of Solutions Architect  | CDN fundamentals, Edge Locations, tối ưu phân phối nội dung toàn cầu bằng CloudFront. |
| **09:30 – 10:45** | Attack Surface Defense: AWS WAF & Application Protection | Julian Ju – Senior Edge Services Specialist SA | WAF, OWASP Top 10, bot mitigation, hạn chế traffic độc hại.                           |
| **10:45 – 12:00** | Lunch & Networking                                       | —                                              | Giao lưu thêm với diễn giả và người tham dự.                                          |
| **13:00 – 14:30** | Hands-On Workshop: Optimize Internet Web Application     | Hưng, Julian, Kevin Lim                        | Cấu hình CloudFront, tối ưu tốc độ ứng dụng Web thực tế.                              |
| **14:45 – 16:15** | Hands-On Workshop: Secure Internet Web Application       | Hưng, Julian, Kevin Lim                        | Thực hành cấu hình WAF rules, block/detect bot, ngăn chặn lỗ hổng OWASP.              |
| **16:15 – 17:00** | Closing & Open Discussion                                | —                                              | Chia sẻ kinh nghiệm, bài học, thảo luận kỹ thuật nâng cao.                            |

## KIẾN THỨC ĐÃ HỌC ĐƯỢC

### 1. CloudFront – Content Delivery & Edge Optimization

* Hiểu bản chất CDN và sự khác biệt giữa Edge Location, Regional Edge Cache và Origin.
* Tối ưu hóa routing và caching để giảm latency, tăng tốc phân phối nội dung trên quy mô toàn cầu.
* Triển khai security layer ngay tại Edge (Origin Shield, Cache policies, Geo restriction).

→ Nhận thức rõ CloudFront không chỉ là CDN, mà còn là lớp bảo vệ và tối ưu nằm trước hệ thống backend.

### 2. AWS WAF – Ứng dụng bảo mật theo lớp

* Nắm được cách dùng WAF để chặn bot, SQL Injection, XSS và các lỗ hổng trong **OWASP Top 10**.
* Thực hành viết rule, điều kiện matching, rate limit, IP allow/deny list.
* Triển khai defense layer giúp giảm tải cho backend, giảm thiểu traffic độc hại.

→ Điểm ấn tượng: dễ dàng tùy chỉnh rule logic phù hợp từng ứng dụng khác nhau.

### 3. Hands-On Labs – Kiến thức thành kỹ năng

* Workshop 1: **Optimize Web Application**
    - Cấu hình CloudFront, Lambda@Edge/Function URL, xác minh hiệu suất trước–sau deploy.
    - Cải thiện cache hit ratio, giảm latency và tăng tốc độ load UI.

* Workshop 2: **Secure Web Application**
    - Thiết kế rule WAF, simulate bot attacks, chặn/giới hạn request.
    - Hiểu rõ cách WAF phân tích request để quyết định block/allow.

→ Học bằng tay là thứ giá trị nhất: thay vì chỉ lý thuyết, được tự cấu hình và thấy kết quả trực tiếp.

## ĐÁNH GIÁ VÀ ỨNG DỤNG TƯƠNG LAI

| Giá trị nhận được             | Ứng dụng thực tế                                               |
|-------------------------------|----------------------------------------------------------------|
| Kiến thức CloudFront nâng cao | Triển khai CDN cho các hệ thống cần tốc độ truy cập toàn cầu.  |
| Nắm AWS WAF chi tiết          | Tăng cường bảo mật app nội bộ, giảm thiểu attack surface.      |
| Kinh nghiệm thực hành         | Rút ngắn thời gian triển khai thực tế, tránh sai sót cấu hình. |
| Networking với SA AWS         | Mở cơ hội học hỏi, trao đổi giải pháp và công nghệ mới.        |

**Next Steps cá nhân:**

1. Xây dựng demo nội bộ xem CloudFront + WAF vận hành chung ra sao.
2. Tự thực hành thêm rule WAF — đặc biệt các use-case bot mitigation & OWASP.
3. Nghiên cứu sâu hơn về Lambda@Edge để xử lý request ở edge layer, giảm tải backend.

## Một số hình ảnh khi tham gia sự kiện.

![](/images/4-Events/Event5.1.jpg)  
![](/images/4-Events/Event5.2.jpg)
![](/images/4-Events/Event5.3.jpg)
![](/images/4-Events/Event5.4.jpg)