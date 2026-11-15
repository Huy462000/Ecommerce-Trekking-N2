# Project Instructions for AI

## 1. Project context
Đây là dự án website thương mại điện tử của sinh viên (học phần Phát triển ứng dụng Web/TMĐT – UEH, Nhóm 2).

- Tên dự án: **Trekaholic** – website đặt tour trekking và cắm trại trực tuyến tại Việt Nam.
- Loại ứng dụng: ứng dụng đặt dịch vụ (Nhóm B), trọng tâm là lịch khởi hành theo đợt, số chỗ trống, giữ chỗ, trạng thái đơn và thanh toán trực tuyến.
- Công nghệ: HTML, CSS, JavaScript, Bootstrap 5; PHP 8; MySQL (kết nối bằng PDO); PHPMailer; chạy trên XAMPP. Thanh toán chỉ dùng VNPay Sandbox. Không tự đổi sang framework hoặc ngôn ngữ khác khi chưa được nhóm đồng ý.
- Tài liệu cần đọc trước khi làm việc: README.md, REQUIREMENTS.md, docs/business-workflow.md, docs/user-roles.md.

## 2. Scope
Chỉ triển khai các chức năng đã được nhóm thống nhất trong REQUIREMENTS.md.

- Ưu tiên chức năng mức "Bắt buộc", sau đó mới đến "Nên có".
- Không triển khai chức năng mức "Nâng cao" hoặc nằm trong mục "Ngoài phạm vi" (ví dụ: nhiều cổng thanh toán, đặt cọc, giỏ hàng nhiều tour, chia tiền nhóm, hoàn tiền tự động, mã giảm giá).
- Không tự thêm chức năng mới. Nếu thấy cần, hãy đề xuất để nhóm quyết định.

## 3. Coding principles
- Giữ mã nguồn dễ đọc và dễ bảo trì.
- Không thay đổi kiến trúc lớn khi chưa được nhóm đồng ý.
- Không tự ý xóa chức năng đang hoạt động.
- Ưu tiên thay đổi nhỏ, có thể kiểm tra.
- Đặt tên biến, hàm, bảng dữ liệu thống nhất và có ý nghĩa.
- Logic giữ chỗ và trạng thái đơn phải theo đúng docs/business-workflow.md.

## 4. Workflow
Trước khi sửa mã nguồn:
1. Đọc các tài liệu liên quan.
2. Phân tích hiện trạng.
3. Đề xuất phương án.
4. Chờ nhóm xác nhận.

Sau khi sửa mã nguồn:
1. Giải thích các thay đổi.
2. Nêu các file đã sửa.
3. Hướng dẫn chạy và kiểm thử.
4. Báo cáo các giới hạn còn tồn tại.

## 5. Security
- Không đưa mật khẩu, API key, token hoặc khóa cổng thanh toán vào mã nguồn; dùng file `.env` và đảm bảo file này có trong `.gitignore`.
- Không tự ý vô hiệu hóa kiểm tra bảo mật (kiểm tra dữ liệu đầu vào, phân quyền, kiểm tra chữ ký thanh toán).
- Không sử dụng dữ liệu cá nhân thật khi chưa được phép; dữ liệu mẫu phải là dữ liệu giả.
- Không thu thập thông tin sức khỏe chi tiết của khách hàng.

## 6. Communication
Nếu yêu cầu chưa rõ, hãy hỏi lại trước khi triển khai.

Trả lời bằng tiếng Việt, ngắn gọn, nêu rõ phần nào đã làm và phần nào chưa làm.
