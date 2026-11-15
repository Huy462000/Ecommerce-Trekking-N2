# Trekaholic – Website đặt tour trekking và cắm trại trực tuyến

## 1. Giới thiệu
Trekaholic là website tìm kiếm và đặt tour leo núi (trekking/hiking) và cắm trại (camping) tại Việt Nam. Khách hàng có thể xem thông tin cung đường đã chuẩn hóa (quãng đường, độ cao, độ khó), xem số chỗ trống theo từng đợt khởi hành, chọn gói dịch vụ (Trọn gói xe đưa đón hoặc Tự túc di chuyển), thuê thêm trang bị và thanh toán trực tuyến.

Vấn đề kinh doanh cần giải quyết:
- Thông tin cung đường (km, độ cao, độ khó) ở nhiều nơi còn phân tán và thiếu chuẩn hóa, người mới khó chọn tour phù hợp.
- Thiếu linh hoạt trong việc tách lẻ gói dịch vụ và khó so sánh giữa các tour.
- Bất tiện khi đặt tour theo nhóm đông người.
- Đặt chỗ thủ công qua Zalo/Fanpage, không biết số chỗ trống, chưa có thanh toán trực tuyến và không lưu lại lịch sử chuyến đi.

## 2. Khách hàng mục tiêu
- Nhân viên văn phòng và giới trẻ (18–40 tuổi) tại các đô thị lớn, muốn trải nghiệm thiên nhiên cuối tuần.
- Người mới bắt đầu, nhóm bạn bè và gia đình cần lịch trình nhẹ nhàng, có hướng dẫn viên.
- Người chạy trail, dân leo núi bán chuyên chỉ cần đặt lẻ dịch vụ.
- Doanh nghiệp, tổ chức có nhu cầu đặt tour teambuilding.

## 3. Chức năng chính
- Xem, tìm kiếm và lọc tour theo địa điểm, cấp độ (Dễ / Trung bình / Khó), thời lượng, giá, ngày khởi hành.
- Xem chi tiết tour: lịch trình, thông số cung đường, dịch vụ bao gồm, chính sách, lịch khởi hành kèm số chỗ trống.
- Đăng ký, đăng nhập, quản lý hồ sơ cá nhân.
- Đặt tour: chọn ngày khởi hành, số người, hạng vé, thuê thêm trang bị; giữ chỗ 15 phút trong lúc thanh toán.
- Thanh toán trực tuyến qua cổng thử nghiệm (Sandbox) và nhận email xác nhận.
- Theo dõi trạng thái đơn, xem lịch sử tour đã đi, gửi yêu cầu hủy/dời tour.
- Gửi yêu cầu tư vấn (dùng cho cả khách doanh nghiệp đặt tour riêng).
- Trang quản trị: quản lý tour, danh mục, lịch khởi hành, số chỗ, đơn đặt và yêu cầu tư vấn.

Chi tiết xem tại [REQUIREMENTS.md](REQUIREMENTS.md).

## 4. Thành viên
| Thành viên | Vai trò |
|---|---|
| Thành Huy | Trưởng nhóm / BA |
| Doanh Doanh | UI/UX |
| Tường Vy | Frontend |
| Ngọc Hà | Backend |
| Long Huy | Database + Thanh toán |
| Hoàng Yến | QA / Integration |

## 5. Công nghệ dự kiến
| Thành phần | Công nghệ | Lý do chọn |
|---|---|---|
| Frontend | HTML, CSS, JavaScript, Bootstrap 5 | Dễ học; Bootstrap giúp làm giao diện responsive nhanh |
| Backend | PHP 8 | Phổ biến trong môn học; VNPay có sẵn code mẫu PHP |
| Cơ sở dữ liệu | MySQL (quản lý bằng phpMyAdmin) | Hỗ trợ transaction để giữ chỗ, chống bán quá số chỗ |
| Kết nối CSDL | PDO, câu lệnh chuẩn bị sẵn (prepared statements) | Chống SQL Injection |
| Thanh toán | VNPay Sandbox | Môi trường thử nghiệm miễn phí, có tài liệu tiếng Việt |
| Gửi email | PHPMailer + Gmail SMTP | Gửi email xác nhận đơn và đặt lại mật khẩu |
| Môi trường chạy | XAMPP (Apache + PHP + MySQL) | Cài một lần là chạy được trên máy mỗi thành viên |
| Thử kết quả thanh toán | ngrok | Cho VNPay gọi về máy cá nhân khi kiểm thử |
| Quản lý mã nguồn | Git, GitHub, VS Code | Làm việc nhóm, quản lý Issue và Pull Request |

## 6. Kế hoạch thực hiện
| Giai đoạn | Nội dung | Thời gian |
|---|---|---|
| 1 | Khảo sát và xác định yêu cầu | Tuần 1–2 |
| 2 | Thiết kế giao diện, cơ sở dữ liệu và API | Tuần 3 |
| 3 | Xây dựng các chức năng frontend | Tuần 4–7 |
| 4 | Phát triển backend và cơ sở dữ liệu | Tuần 4–8 |
| 5 | Tích hợp và kiểm thử | Tuần 9–10 |
| 6 | Triển khai, hoàn thiện, chức năng bổ sung | Tuần 11–12 |

Chi tiết xem tại [PROJECT_PLAN.md](PROJECT_PLAN.md).

## 7. Liên kết
- Bảng yêu cầu: [REQUIREMENTS.md](REQUIREMENTS.md)
- Kế hoạch: [PROJECT_PLAN.md](PROJECT_PLAN.md)
- Phân tích website: [docs/competitor-analysis.md](docs/competitor-analysis.md)
- Vai trò người dùng: [docs/user-roles.md](docs/user-roles.md)
- Quy trình nghiệp vụ: [docs/business-workflow.md](docs/business-workflow.md)
- Nguyên tắc dùng AI: [AGENTS.md](AGENTS.md)
- Nhật ký dùng AI: [AI_USAGE_LOG.md](AI_USAGE_LOG.md)
