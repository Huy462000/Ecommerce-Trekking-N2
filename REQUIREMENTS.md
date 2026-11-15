# Requirements

## 1. Mục tiêu dự án

**Mục tiêu kinh doanh**
- Chuẩn hóa thông tin cung đường trekking/camping (quãng đường, độ cao tích lũy, độ khó) để khách chọn được tour phù hợp thể lực.
- Tự động hóa quy trình đặt chỗ: hiển thị số chỗ trống theo từng đợt, giữ chỗ, thanh toán trực tuyến và gửi xác nhận, thay cho việc chốt đơn thủ công qua Zalo/Fanpage.
- Lưu lại lịch sử tour của khách hàng, làm cơ sở cho ưu đãi khách cũ.

**Giá trị mang lại cho khách hàng**
- Biết rõ tour có hợp sức mình không trước khi đặt.
- Biết ngay đợt nào còn chỗ, đặt và thanh toán trong vài phút.
- Linh hoạt chọn gói Trọn gói xe đưa đón hoặc Tự túc di chuyển, thuê thêm trang bị.
- Xem lại các tour đã đi và nhận ưu đãi khi quay lại.

## 2. Phạm vi

### Trong phạm vi
- Xem, tìm kiếm, lọc tour; xem chi tiết tour và lịch khởi hành kèm số chỗ trống.
- Đăng ký, đăng nhập, quên mật khẩu, quản lý hồ sơ cá nhân.
- Đặt tour (bắt buộc đăng nhập): chọn đợt, số người, hạng vé, thuê trang bị; giỏ hàng gồm 1 tour và trang bị thuê kèm.
- Giữ chỗ 15 phút trong lúc chờ thanh toán.
- Thanh toán trực tuyến qua VNPay Sandbox; email xác nhận kèm mã đặt chỗ.
- Theo dõi trạng thái đơn, xem lịch sử tour, gửi yêu cầu hủy/dời tour.
- Gửi và xử lý yêu cầu tư vấn (kể cả yêu cầu tour riêng của doanh nghiệp).
- Trang quản trị cho Quản trị hệ thống và Nhân viên điều hành / tư vấn.
- Chức năng mức "Nên có" (tuần 11–12 nếu còn thời gian): đánh giá sau chuyến đi, ưu đãi khách cũ, blog/FAQ, báo cáo thống kê, vai trò Marketing.

### Ngoài phạm vi
- Ứng dụng di động (iOS/Android).
- Đặt tour không cần tài khoản.
- Đặt cọc nhiều lần; nhiều cổng thanh toán; đối soát dòng tiền thật với ngân hàng.
- Hoàn tiền tự động theo % (Admin xử lý thủ công).
- Giỏ hàng chứa nhiều tour cùng lúc.
- Chia tiền nhóm, link đặt nhóm.
- Chuyển nhượng đơn.
- Lưu thông tin sức khỏe chi tiết của khách.
- So sánh tour.
- Mã giảm giá, hạng thành viên, SEO.
- Phân bổ xe, lều, hướng dẫn viên; gửi thông báo hàng loạt; tạo đơn thay khách; xử lý khiếu nại.
- Vai trò Hướng dẫn viên và Đối tác; cổng riêng cho đối tác.
- Theo dõi vị trí GPS.

## 3. Người dùng

| Vai trò | Mô tả | Quyền hạn |
|---|---|---|
| Khách chưa đăng nhập | Người truy cập website | Xem thông tin công khai (tour, lịch khởi hành, giá, chính sách); đăng ký/đăng nhập; gửi yêu cầu tư vấn |
| Khách hàng | Người đã có tài khoản | Đặt tour, thanh toán, theo dõi đơn, xem lịch sử tour, gửi yêu cầu hủy/dời, đánh giá sau tour, quản lý hồ sơ cá nhân |
| Quản trị hệ thống | Người quản lý toàn bộ hệ thống | Toàn quyền: tạo và phân quyền tài khoản nội bộ; quản lý tour, danh mục, lịch khởi hành, giá, đơn đặt, tài khoản khách hàng; xem báo cáo |
| Nhân viên điều hành và tư vấn | Nhân viên vận hành tour | Mở/đóng/hoãn lịch khởi hành; xem danh sách khách theo chuyến; trả lời yêu cầu tư vấn; xử lý yêu cầu hủy/dời |
| Marketing _(Nên có)_ | Nhân viên nội dung | Đăng bài viết, cập nhật banner, duyệt đánh giá |

Mỗi nhân viên nội bộ dùng tài khoản riêng, không dùng chung.

## 4. Yêu cầu chức năng

Mức độ ưu tiên: **Bắt buộc** = làm xong trong tuần 1–10; **Nên có** = tuần 11–12 nếu còn thời gian; **Nâng cao** = để sau học phần (không làm trong đồ án).

### 4.1. Khách chưa đăng nhập

| Mã | Tên chức năng | Mô tả | Người sử dụng | Ưu tiên | Tiêu chí nghiệm thu |
|---|---|---|---|---|---|
| F01 | Xem danh sách tour | Hiển thị danh sách tour đang mở bán, mỗi tour có ảnh, tên, cấp độ, thời lượng, giá từ | Khách chưa đăng nhập | Bắt buộc | Trang hiển thị đủ các tour đang mở; tour bị ẩn không xuất hiện |
| F02 | Xem chi tiết tour | Lịch trình theo ngày, quãng đường, độ cao, độ khó, giá, dịch vụ bao gồm, chính sách hủy/dời, lịch khởi hành kèm số chỗ trống | Khách chưa đăng nhập | Bắt buộc | Mỗi đợt hiển thị đúng số chỗ trống; đợt hết chỗ hiện "Hết chỗ" và không chọn được |
| F03 | Tìm kiếm và lọc tour | Tìm theo từ khóa; lọc kết hợp theo cấp độ, địa điểm, giá, ngày khởi hành | Khách chưa đăng nhập | Bắt buộc | Chọn nhiều điều kiện thì chỉ hiện tour thỏa tất cả; không có kết quả thì hiện thông báo |
| F04 | Xem chính sách, FAQ, blog, đánh giá | Trang chính sách và FAQ dạng trang tĩnh; blog và đánh giá nếu có | Khách chưa đăng nhập | Nên có | Truy cập được từ menu; nội dung hiển thị đúng |
| F05 | Đăng ký tài khoản | Đăng ký bằng họ tên, email, số điện thoại, mật khẩu | Khách chưa đăng nhập | Bắt buộc | Email hoặc SĐT đã tồn tại thì báo lỗi; mật khẩu được mã hóa khi lưu |
| F06 | Đăng nhập, quên mật khẩu | Đăng nhập bằng email/SĐT và mật khẩu; đặt lại mật khẩu qua email | Khách chưa đăng nhập | Bắt buộc | Sai mật khẩu thì báo lỗi; link đặt lại mật khẩu chỉ dùng được 1 lần |
| F07 | Gửi form yêu cầu tư vấn | Gửi họ tên, SĐT, nội dung (dùng cả cho doanh nghiệp đặt tour riêng) | Khách chưa đăng nhập | Bắt buộc | Gửi xong hiện thông báo thành công; yêu cầu xuất hiện trong trang quản trị (F31) |

### 4.2. Khách hàng

| Mã | Tên chức năng | Mô tả | Người sử dụng | Ưu tiên | Tiêu chí nghiệm thu |
|---|---|---|---|---|---|
| F08 | Quản lý hồ sơ cá nhân | Cập nhật thông tin liên hệ và liên hệ khẩn cấp. Không lưu thông tin sức khỏe chi tiết | Khách hàng | Bắt buộc | Lưu thành công thì hiện dữ liệu mới; SĐT sai định dạng thì báo lỗi |
| F09 | Chọn tour, ngày khởi hành, số người | Chọn đợt còn chỗ, số người, hạng vé (Trọn gói / Tự túc) và trang bị thuê kèm | Khách hàng | Bắt buộc | Không chọn được số người lớn hơn số chỗ trống |
| F10 | Đặt chỗ tour | Hệ thống tự tính giá: giá hạng vé × số người + tiền thuê trang bị | Khách hàng | Bắt buộc | Tổng tiền hiển thị đúng công thức; đổi số người hoặc trang bị thì tổng tiền cập nhật |
| F11 | Xác nhận miễn trừ trách nhiệm | Tick đồng ý điều khoản miễn trừ trách nhiệm và xác nhận đủ sức khỏe cho cấp độ tour | Khách hàng | Nên có | Chưa tick thì không bấm được nút thanh toán |
| F12 | Thanh toán trực tuyến | Thanh toán đủ một lần qua VNPay Sandbox | Khách hàng | Bắt buộc | Thanh toán thành công thì đơn chuyển "Đã xác nhận"; thất bại thì đơn vẫn "Chờ thanh toán" và được thanh toán lại |
| F13 | Theo dõi đơn và lịch sử tour | Xem trạng thái các đơn; danh sách tour đã hoàn thành | Khách hàng | Bắt buộc | Chỉ thấy đơn của chính mình; đơn "Hoàn thành" hiện trong lịch sử tour |
| F14 | Gửi yêu cầu hủy hoặc dời đơn | Gửi yêu cầu theo chính sách, trước ngày khởi hành | Khách hàng | Bắt buộc | Đơn chuyển sang "Yêu cầu hủy/dời"; sau ngày khởi hành thì không gửi được |
| F15 | Đánh giá tour sau chuyến đi | Chấm điểm và nhận xét | Khách hàng | Nên có | Chỉ đơn "Hoàn thành" mới được đánh giá; mỗi đơn đánh giá 1 lần |
| F16 | Tích lũy lượt đi, nhận hạng | Xếp hạng thành viên theo số tour đã đi | Khách hàng | Nâng cao | Không làm trong đồ án |
| F39 | Giỏ hàng | Giỏ chỉ gồm 1 tour và trang bị thuê kèm; thêm, sửa, xóa trang bị trước khi thanh toán | Khách hàng | Bắt buộc | Thêm tour khác thì thay tour cũ trong giỏ; tổng tiền cập nhật đúng |
| F40 | Giữ chỗ 15 phút | Khi tạo đơn, hệ thống giữ chỗ 15 phút chờ thanh toán | Khách hàng | Bắt buộc | Đợt còn 1 chỗ: khách A tạo đơn thì khách B thấy hết chỗ; quá 15 phút A chưa trả thì chỗ được mở lại |
| F41 | Email xác nhận đơn | Gửi email kèm mã đặt chỗ sau khi thanh toán thành công | Khách hàng | Bắt buộc | Email đến đúng địa chỉ, có mã đặt chỗ, tên tour, ngày khởi hành, số tiền |
| F42 | Ưu đãi khách cũ | Khách có ít nhất 1 đơn "Hoàn thành" được tự động giảm giá cho đơn mới (1 loại ưu đãi, không cộng dồn) | Khách hàng | Nên có | Khách mới không được giảm; khách cũ thấy dòng giảm giá trong tổng tiền |

### 4.3. Quản trị hệ thống

| Mã | Tên chức năng | Mô tả | Người sử dụng | Ưu tiên | Tiêu chí nghiệm thu |
|---|---|---|---|---|---|
| F17 | Tạo tài khoản nội bộ và phân quyền | Tạo tài khoản cho nhân viên, gán vai trò | Quản trị hệ thống | Bắt buộc | Nhân viên điều hành không vào được chức năng chỉ dành cho Quản trị |
| F18 | Cấu hình hệ thống và cổng thanh toán | Giao diện cấu hình | Quản trị hệ thống | Nâng cao | Không làm; cấu hình để trong file `.env` |
| F19 | Nhật ký hoạt động, sao lưu | Xem log, sao lưu dữ liệu | Quản trị hệ thống | Nâng cao | Không làm trong đồ án |
| F20 | Quản lý tour | Thêm, sửa, ẩn, xóa tour; upload ảnh | Quản trị hệ thống | Bắt buộc | Tour bị ẩn không hiện ở trang khách; tour đã có đơn thì không xóa được, chỉ ẩn |
| F21 | Quản lý danh mục | Quản lý cấp độ, địa điểm | Quản trị hệ thống | Bắt buộc | Danh mục mới xuất hiện trong bộ lọc F03 |
| F22 | Quản lý lịch khởi hành và giá | Tạo đợt khởi hành, số chỗ, giá từng hạng vé | Quản trị hệ thống | Bắt buộc | Không giảm số chỗ xuống thấp hơn số chỗ đã bán |
| F23 | Quản lý đơn đặt | Xem đơn; xác nhận, hủy, ghi nhận hoàn tiền thủ công | Quản trị hệ thống | Bắt buộc | Đổi trạng thái đúng theo quy trình ở docs/business-workflow.md |
| F24 | Quản lý tài khoản khách hàng | Xem, khóa tài khoản khách | Quản trị hệ thống | Nên có | Tài khoản bị khóa không đăng nhập được |
| F25 | Báo cáo thống kê | Doanh thu và số khách theo tháng (dạng bảng) | Quản trị hệ thống | Nên có | Số liệu khớp với các đơn "Đã xác nhận" và "Hoàn thành" |

### 4.4. Nhân viên điều hành và tư vấn

| Mã | Tên chức năng | Mô tả | Người sử dụng | Ưu tiên | Tiêu chí nghiệm thu |
|---|---|---|---|---|---|
| F26 | Mở, đóng, hoãn lịch khởi hành | Đổi trạng thái đợt; đặt số khách tối thiểu/tối đa | Nhân viên điều hành | Bắt buộc | Đợt "Đóng" hoặc "Hoãn" thì khách không đặt được |
| F27 | Xem danh sách khách theo chuyến | Danh sách người đi của từng đợt | Nhân viên điều hành | Bắt buộc | Chỉ hiện khách của đơn "Đã xác nhận" |
| F28 | Phân bổ xe, lều, hướng dẫn viên | Điều phối hậu cần | Nhân viên điều hành | Nâng cao | Không làm trong đồ án |
| F29 | Thông báo hàng loạt cho đoàn | Gửi thông báo khi chốt/hoãn tour | Nhân viên điều hành | Nâng cao | Không làm trong đồ án |
| F30 | Tạo đơn thay khách | Nhân viên đặt tour giúp khách | Nhân viên tư vấn | Nâng cao | Không làm trong đồ án |
| F31 | Tiếp nhận và trả lời yêu cầu tư vấn | Xem danh sách yêu cầu từ F07, đánh dấu đã xử lý | Nhân viên tư vấn | Bắt buộc | Yêu cầu mới hiện đầu danh sách; đánh dấu xong thì chuyển trạng thái "Đã xử lý" |
| F32 | Xử lý yêu cầu hủy, dời | Duyệt hoặc từ chối yêu cầu từ F14 | Nhân viên tư vấn | Bắt buộc | Duyệt hủy thì đơn chuyển "Cần hoàn tiền"; duyệt dời thì đơn gắn với đợt mới |
| F33 | Xử lý khiếu nại | Quản lý khiếu nại của khách | Nhân viên tư vấn | Nâng cao | Không làm trong đồ án |

### 4.5. Marketing

| Mã | Tên chức năng | Mô tả | Người sử dụng | Ưu tiên | Tiêu chí nghiệm thu |
|---|---|---|---|---|---|
| F34 | Quản lý bài viết kinh nghiệm | Đăng, sửa, ẩn bài viết | Marketing | Nên có | Bài bị ẩn không hiện ở trang khách |
| F35 | Cập nhật banner trang chủ | Thay ảnh và liên kết banner | Marketing | Nên có | Banner mới hiện ở trang chủ |
| F36 | Quản lý mã giảm giá | Tạo mã khuyến mãi | Marketing | Nâng cao | Không làm trong đồ án |
| F37 | Thiết lập SEO | Tiêu đề, mô tả cho tour và bài viết | Marketing | Nâng cao | Không làm trong đồ án |
| F38 | Duyệt hoặc ẩn đánh giá | Ẩn đánh giá không phù hợp | Marketing | Nên có | Đánh giá bị ẩn không hiện ở trang chi tiết tour |

## 5. Yêu cầu phi chức năng
- **Giao diện:** đáp ứng nhiều kích thước màn hình (máy tính và điện thoại, từ 360px).
- **Kiểm tra dữ liệu đầu vào:** kiểm tra ở cả trình duyệt và máy chủ; chống SQL Injection và XSS.
- **Phân quyền:** các trang quản trị yêu cầu đăng nhập và đúng vai trò; khách chỉ xem được đơn của mình.
- **Toàn vẹn dữ liệu:** không bán quá số chỗ khi nhiều người đặt cùng lúc (dùng transaction khi tạo đơn).
- **Bảo mật thanh toán:** kiểm tra chữ ký kết quả trả về từ VNPay, đối chiếu số tiền; cùng một kết quả gửi lại 2 lần không xử lý 2 lần.
- **Mật khẩu:** được mã hóa (bcrypt hoặc tương đương), không lưu dạng chữ thường.
- **Mã nguồn:** tổ chức rõ ràng theo thư mục; đặt tên thống nhất.
- **Không công khai thông tin bí mật:** API key, mật khẩu, khóa cổng thanh toán để trong file `.env` và có trong `.gitignore`.
- **Quyền riêng tư:** chỉ thu thập dữ liệu cần thiết; dữ liệu mẫu trong repo là dữ liệu giả.
- **Hiệu năng:** trang danh sách và chi tiết tour tải dưới 2 giây với dữ liệu mẫu 30–50 tour.

## 6. Giới hạn và giả định
- **Thời gian:** 1 học phần, khoảng 12 tuần; tuần 1–10 cho chức năng "Bắt buộc", tuần 11–12 cho "Nên có".
- **Nguồn lực:** 6 thành viên; 1 người phụ trách chính cho mỗi mảng Frontend, Backend, Database + Thanh toán.
- **Công nghệ:** HTML/CSS/JavaScript (Bootstrap 5), PHP 8, MySQL, chạy trên XAMPP (chi tiết tại README.md). Thanh toán chỉ dùng môi trường thử nghiệm VNPay Sandbox, không giao dịch tiền thật.
- **Mô hình vận hành:** Trekaholic tự tổ chức tour; toàn bộ dữ liệu tour do quản trị viên nhập. Dữ liệu mẫu gồm 30–50 tour phủ cả 3 miền.
- **Thang độ khó:** Dễ / Trung bình / Khó, xác định theo quãng đường và độ cao tích lũy (nhóm chốt ngưỡng cụ thể).
- **Giả định:** khách có email và số điện thoại hợp lệ; tour có ngày khởi hành cố định.
