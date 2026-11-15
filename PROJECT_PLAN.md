# Project Plan

## 1. Thành viên và vai trò

| Thành viên | Vai trò | Trách nhiệm | Sản phẩm phụ trách |
|---|---|---|---|
| Thành Huy | Trưởng nhóm / BA | Quản lý tiến độ, yêu cầu, GitHub Issues và điều phối nhóm | REQUIREMENTS.md, PROJECT_PLAN.md |
| Doanh Doanh | UI/UX | Khảo sát giao diện, đề xuất thiết kế và chuẩn bị tài nguyên | docs/competitor-analysis.md (phần giao diện), bản phác thảo |
| Tường Vy | Frontend | Xây dựng giao diện HTML/CSS/JavaScript | Trang danh sách, chi tiết, form đặt tour; docs/user-roles.md |
| Ngọc Hà | Backend | Thiết kế dữ liệu, nghiệp vụ và API | API và logic số chỗ |
| Long Huy | Database + Thanh toán | Thiết kế CSDL, tích hợp thanh toán | Sơ đồ CSDL, luồng thanh toán |
| Hoàng Yến | QA / Integration | Lập kế hoạch kiểm thử, kiểm tra tích hợp và tài liệu | Test plan, docs/business-workflow.md |

## 2. Các giai đoạn
- **Giai đoạn 1 (Tuần 1–2): Khảo sát và xác định yêu cầu.** Phân tích 3 website, xác định vai trò, chức năng, quy trình; dùng AI phân tích và phản biện; tạo repository.
- **Giai đoạn 2 (Tuần 3): Thiết kế giao diện.** Phác thảo các trang chính; chốt sơ đồ CSDL và danh sách API.
- **Giai đoạn 3 (Tuần 4–7): Xây dựng các chức năng frontend.** Trang chủ, danh sách, chi tiết, đăng ký/đăng nhập, giỏ hàng, form đặt tour, trang quản trị.
- **Giai đoạn 4 (Tuần 4–8): Phát triển backend và cơ sở dữ liệu.** API tour, lịch khởi hành, giữ chỗ, đơn hàng, thanh toán VNPay, email.
- **Giai đoạn 5 (Tuần 9–10): Tích hợp và kiểm thử.** Ghép frontend với backend, kiểm thử theo tiêu chí nghiệm thu, sửa lỗi.
- **Giai đoạn 6 (Tuần 11–12): Triển khai và hoàn thiện.** Triển khai bản demo, làm chức năng "Nên có" nếu còn thời gian, hoàn thiện tài liệu và báo cáo.

## 3. Công việc

| Mã | Công việc | Người phụ trách | Kết quả cần đạt | Thời hạn | Trạng thái |
|---|---|---|---|---|---|
| T01 | Khởi tạo repository, chốt yêu cầu nghiệp vụ và quy chuẩn AI (Issue #1) | Thành Huy | README.md, REQUIREMENTS.md, PROJECT_PLAN.md, AGENTS.md | Tuần 1 | Đang làm |
| T02 | Khảo sát 3 website đối thủ và phân tích giao diện (Issue #2) | Doanh Doanh | docs/competitor-analysis.md | Tuần 1 | Hoàn thành |
| T03 | Xác định vai trò người dùng và danh sách chức năng (Issue #3) | Tường Vy | docs/user-roles.md | Tuần 1 | Hoàn thành |
| T04 | Xây dựng quy trình đặt tour và kế hoạch kiểm thử (Issue #4) | Hoàng Yến | docs/business-workflow.md, test plan bản đầu | Tuần 2 | Đang làm |
| T05 | Xác định kiến trúc API và logic lịch khởi hành, giữ chỗ (Issue #5) | Ngọc Hà | Danh sách API, mô tả logic giữ chỗ 15 phút | Tuần 3 | Chưa làm |
| T06 | Thiết kế CSDL (ERD) và luồng thanh toán Sandbox (Issue #6) | Long Huy | Sơ đồ ERD, sơ đồ luồng thanh toán | Tuần 3 | Chưa làm |
| T07 | Ghi nhật ký sử dụng AI | Thành Huy | AI_USAGE_LOG.md | Tuần 1 | Đang làm |
| T08 | Phác thảo giao diện các trang chính | Doanh Doanh | Bản thiết kế trang chủ, danh sách, chi tiết, đặt tour, quản trị | Tuần 3 | Chưa làm |
| T09 | Giao diện trang chủ, danh sách, chi tiết, tìm kiếm/lọc | Tường Vy | Trang F01–F03 chạy với dữ liệu mẫu | Tuần 5 | Chưa làm |
| T10 | Đăng ký, đăng nhập, hồ sơ, phân quyền | Ngọc Hà, Tường Vy | F05, F06, F08, F17 | Tuần 6 | Chưa làm |
| T11 | Quản lý tour, danh mục, lịch khởi hành | Ngọc Hà, Tường Vy | F20, F21, F22, F26 | Tuần 6 | Chưa làm |
| T12 | Giỏ hàng, đặt tour, giữ chỗ 15 phút | Ngọc Hà | F09, F10, F39, F40 đạt tiêu chí nghiệm thu | Tuần 7 | Chưa làm |
| T13 | Tích hợp VNPay Sandbox và email xác nhận | Long Huy | F12, F41 | Tuần 8 | Chưa làm |
| T14 | Theo dõi đơn, lịch sử tour, hủy/dời, tư vấn | Ngọc Hà, Tường Vy | F07, F13, F14, F23, F27, F31, F32 | Tuần 8 | Chưa làm |
| T15 | Dữ liệu mẫu 30–50 tour | Hoàng Yến, Doanh Doanh | File dữ liệu mẫu (dữ liệu giả) | Tuần 4 | Chưa làm |
| T16 | Kiểm thử tích hợp và sửa lỗi | Hoàng Yến (cả nhóm) | Báo cáo kiểm thử; lỗi nghiêm trọng đã sửa | Tuần 10 | Chưa làm |
| T17 | Chức năng "Nên có" | Cả nhóm | F04, F11, F15, F24, F25, F34, F35, F38, F42 (nếu kịp) | Tuần 12 | Chưa làm |
| T18 | Triển khai demo và hoàn thiện báo cáo | Thành Huy, Hoàng Yến | Bản demo chạy được, báo cáo cuối kỳ | Tuần 12 | Chưa làm |

## 4. Rủi ro

| Rủi ro | Mức độ | Phương án xử lý |
|---|---|---|
| Lỗi tích hợp VNPay, không nhận được kết quả trả về khi chạy trên máy cá nhân | Cao | Dùng VNPay Sandbox kèm công cụ tạo đường hầm (ngrok); có nút giả lập thành công/thất bại để kiểm thử và demo |
| Bán quá số chỗ khi nhiều người đặt cùng lúc | Trung bình | Giữ chỗ khi tạo đơn trong transaction của CSDL; đơn quá 15 phút tự hết hiệu lực |
| Ôm đồm quá nhiều chức năng, trễ tiến độ | Cao | Chỉ làm chức năng "Bắt buộc" ở tuần 1–10; chức năng "Nâng cao" không làm; giỏ hàng chỉ 1 tour; chỉ 1 cổng thanh toán |
| Frontend và Backend bị quá tải (mỗi mảng 1 người) | Cao | UI/UX hỗ trợ dựng HTML/CSS; QA chuẩn bị dữ liệu mẫu và kiểm thử từ tuần 4 |
| Xung đột mã nguồn, lệch cấu trúc dữ liệu giữa Frontend và Backend | Trung bình | Chốt sơ đồ CSDL và danh sách API trước tuần 3; mỗi chức năng một nhánh Git; Pull Request phải được người khác kiểm tra trước khi gộp |
| Yêu cầu thay đổi giữa chừng | Trung bình | Mọi thay đổi phải cập nhật REQUIREMENTS.md sau khi nhóm đồng ý; ghi lại trong AI_USAGE_LOG.md nếu có dùng AI |
| Lộ khóa thanh toán, mật khẩu trên repository công khai | Cao | Lưu trong file `.env`, thêm vào `.gitignore`; kiểm tra trước mỗi lần push |
