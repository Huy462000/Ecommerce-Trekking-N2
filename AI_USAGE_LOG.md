# AI Usage Log

Nhật ký ghi lại việc nhóm 2 dùng công cụ AI để phân tích yêu cầu trong dự án **Trekaholic**. Quy trình áp dụng: AI thứ nhất phân tích, AI thứ hai phản biện, nhóm thảo luận và quyết định, sau đó mới cập nhật tài liệu.

## Lần sử dụng 1

### Công cụ

Tên công cụ AI: Gemini (Google)

### Mục đích

Phân tích yêu cầu dự án (Nhiệm vụ 3): đề xuất mục tiêu, phạm vi, vai trò người dùng, danh sách chức năng, quy trình nghiệp vụ, yêu cầu phi chức năng và rủi ro.

### Prompt

```text
Bạn là chuyên gia phân tích nghiệp vụ cho dự án thương mại điện tử.
Thông tin dự án:
- Tên dự án: Trekaholic – Website đặt tour trekking và cắm trại trực tuyến tại Việt Nam
- Dịch vụ: Nền tảng tìm kiếm và đặt dịch vụ tour du lịch trải nghiệm, leo núi (trekking/hiking) và cắm trại (camping) toàn quốc, phân loại theo cấp độ thể lực (dễ, trung bình, khó) và thời lượng (1N, 2N1Đ, 2N2Đ, 3N2Đ). Hỗ trợ tùy biến gói dịch vụ (Trọn gói xe đưa đón hoặc Tự túc di chuyển) và thuê thêm trang bị đi rừng.
- Khách hàng mục tiêu: Nhân viên văn phòng & giới trẻ (18–40 tuổi) tại các đô thị lớn có nhu cầu trải nghiệm thiên nhiên cuối tuần; người mới bắt đầu (beginners) & nhóm bạn bè/gia đình; người chạy trail/leo núi bán chuyên cần dịch vụ lẻ; doanh nghiệp/tổ chức đặt tour teambuilding.
- Vấn đề kinh doanh:
  1. Thông tin cung đường (quãng đường km, độ cao, độ khó) ở nhiều nơi còn phân tán và thiếu chuẩn hóa, khiến người mới khó chọn tour phù hợp.
  2. Thiếu linh hoạt trong việc tách lẻ gói dịch vụ (có/không xe đưa đón) và khó so sánh ngang hàng giữa các tour.
  3. Bất tiện khi đăng ký đặt tour theo nhóm đông người (gom thông tin cá nhân, bảo hiểm, thuê đồ.
  4. Quy trình đặt chỗ thủ công qua tin nhắn fanpage/Zalo, khó theo dõi số chỗ trống (slot) theo thời gian thực, thiếu thanh toán trực tuyến tự động và lịch sử lưu vết hành trình của khách hàng.
- Website tham khảo: https://toongadventure.com/, https://itrek.vn/, https://www.dichungxe.net/
- Thời gian thực hiện: 1 học phần (khoảng 10 – 12 tuần)
- Quy mô nhóm: 6 thành viên (Trưởng nhóm/BA, UI/UX, Frontend, Backend, Database + Thanh toán, QA/Integration)
Hãy đề xuất:
1. Mục tiêu và phạm vi dự án.
2. Các nhóm người dùng và quyền hạn.
3. Danh sách chức năng cần có.
4. Quy trình nghiệp vụ chính.
5. Yêu cầu phi chức năng.
6. Các chức năng nên hoàn thành ở phiên bản đầu tiên.
7. Các chức năng nâng cao có thể bổ sung.
8. Rủi ro khi triển khai và cách giảm thiểu.
Phân biệt rõ:
- Yêu cầu bắt buộc.
- Yêu cầu có thể phát triển sau.
- Đề xuất cần nhóm xác minh thêm.
Không giả định nhóm có đủ thời gian hoặc năng lực để triển khai tất cả chức năng. Hãy giải thích cơ sở của từng đề xuất.
```

### Kết quả đề xuất

- **Phạm vi:** web responsive; tìm kiếm, lọc, so sánh tour; đặt tour cho cá nhân và nhóm; thanh toán Sandbox; tra cứu đơn bằng mã đặt chỗ; lịch sử chuyến đi (Trekking Passport); trang quản trị.
- **Vai trò:** Khách vãng lai, Thành viên, Admin (gộp quản trị và điều hành vào 1 tài khoản). Hướng dẫn viên, Marketing, Đối tác để phát triển sau.
- **Chức năng bắt buộc:** phân loại danh mục; tìm kiếm, lọc, so sánh 3 tour; chi tiết tour và lịch khởi hành kèm số chỗ; đặt tour (hạng vé, thuê trang bị, thông tin người đi cùng, miễn trừ trách nhiệm); thanh toán VNPay Sandbox hoặc VietQR; tra cứu đơn và Trekking Passport; Admin quản lý tour, lịch, số chỗ, đơn, xuất danh sách khách.
- **Phát triển sau:** chia tiền nhóm, đánh giá xác thực, tích điểm và ưu đãi khách cũ.
- **Cần xác minh:** hoàn/hủy và dời lịch (duyệt thủ công hay hoàn tiền tự động), khóa chỗ tạm 15 phút.
- **Rủi ro:** lỗi tích hợp cổng thanh toán, bán quá số chỗ, ôm đồm chức năng, xung đột mã nguồn.

### Phản biện

Kết quả được phản biện bằng Claude ở Lần sử dụng 2.

### Quyết định của nhóm

| Mục trong đề xuất của Gemini    | Nội dung                                                   | Quyết định của nhóm                                                                                      |
| ------------------------------- | ---------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| 1. Mục tiêu                     | Mục tiêu kinh doanh                                        | Phù hợp với định hướng của nhóm                                                                          |
| 1. Mục tiêu                     | Mục tiêu học thuật và kỹ thuật                             | Phù hợp với định hướng của nhóm                                                                          |
| 1. Phạm vi                      | Trong phạm vi – yêu cầu bắt buộc                           | Phù hợp với định hướng của nhóm, nhưng cần bổ sung mô tả yêu cầu cho điều phối viên, tư vấn và marketing |
| 1. Phạm vi                      | Ngoài phạm vi                                              | Có thể triển khai trong thời gian tới                                                                    |
| 2. Người dùng                   | Khách vãng lai (Guest)                                     | Không phù hợp định hướng của nhóm                                                                        |
| 2. Người dùng                   | Khách hàng thành viên (Member)                             | Đồng ý, trừ phần theo dõi tổng km đã chinh phục (Trekking Passport) không phù hợp định hướng của nhóm    |
| 2. Người dùng                   | Quản trị viên / Điều hành (Admin)                          | Không gộp; nhóm tách vai trò Quản trị viên và Người điều hành, tư vấn tour                               |
| 2. Người dùng                   | Hướng dẫn viên / Marketing / Đối tác                       | Đồng ý (phát triển sau)                                                                                  |
| 3A. Bắt buộc                    | 1. Phân loại và hiển thị danh mục tour                     | Đồng ý                                                                                                   |
| 3A. Bắt buộc                    | 2. Tìm kiếm, lọc đa tiêu chí và so sánh tour               | Đồng ý                                                                                                   |
| 3A. Bắt buộc                    | 3. Chi tiết tour và lịch khởi hành                         | Đồng ý                                                                                                   |
| 3A. Bắt buộc                    | 4. Đặt tour và tùy biến dịch vụ                            | Đồng ý                                                                                                   |
| 3A. Bắt buộc                    | 5. Thanh toán trực tuyến (Sandbox) và cấp Booking Code     | Cân nhắc thực hiện tích hợp cổng thanh toán phù hợp                                                      |
| 3A. Bắt buộc                    | 6. Tra cứu đơn và hành trình cá nhân (Trekking Passport)   | Đồng ý                                                                                                   |
| 3A. Bắt buộc                    | 7. Trang quản trị (Admin Dashboard)                        | Đồng ý                                                                                                   |
| 3B. Phát triển sau              | 1. Chia sẻ link đặt nhóm và chia tiền                      | Đồng ý                                                                                                   |
| 3B. Phát triển sau              | 2. Đánh giá xác thực sau chuyến đi                         | Đồng ý                                                                                                   |
| 3B. Phát triển sau              | 3. Tích điểm và tự động áp mã ưu đãi                       | Đồng ý                                                                                                   |
| 3C. Cần xác minh                | 1. Quy trình xử lý hoàn/hủy và dời lịch                    | Đồng ý                                                                                                   |
| 3C. Cần xác minh                | 2. Cơ chế khóa chỗ tạm thời                                | Đồng ý                                                                                                   |
| 4. Quy trình nghiệp vụ chính    | Luồng đặt tour trực tuyến                                  | Đồng ý                                                                                                   |
| 5. Yêu cầu phi chức năng        | Toàn vẹn dữ liệu, tương thích thiết bị, bảo mật, hiệu năng | Đồng ý                                                                                                   |
| 6. Chức năng phiên bản đầu tiên | Phân hệ khách hàng, đặt tour và thanh toán, quản trị       | Đồng ý                                                                                                   |
| 7. Chức năng nâng cao           | Đánh giá, đếm ngược giữ chỗ, link đặt nhóm, xuất Excel     | Đồng ý                                                                                                   |
| 8. Rủi ro                       | Các rủi ro và cách giảm thiểu                              | Đồng ý                                                                                                   |

---

## Lần sử dụng 2

### Công cụ

Tên công cụ AI: Claude (Anthropic)

### Mục đích

Phản biện độc lập danh sách yêu cầu do Gemini đề xuất (Nhiệm vụ 4).

### Prompt

```text
Bạn là người phản biện độc lập cho một dự án website thương mại điện tử do nhóm 6 sinh viên thực hiện trong 1 học phần (10–12 tuần).
Tôi sẽ cung cấp thông tin dự án dưới đây:

1. Mô tả đề tài:
- Tên dự án: Trekaholic – Website đặt tour trekking và cắm trại trực tuyến tại Việt Nam.
- Dịch vụ: Tìm kiếm và đặt tour leo núi (trekking/hiking) và cắm trại (camping) toàn quốc; phân loại theo cấp độ thể lực (Dễ, Trung bình, Khó) và thời lượng (1N, 2N1Đ, 2N2Đ, 3N2Đ); hỗ trợ tùy biến gói dịch vụ (Trọn gói xe đưa đón / Tự túc di chuyển) và thuê thêm trang bị đi rừng.

2. Vấn đề kinh doanh và khách hàng mục tiêu:
- Khách hàng mục tiêu: Nhân viên văn phòng & giới trẻ (18–50 tuổi) tại đô thị lớn; người mới bắt đầu (beginners) & nhóm bạn bè/gia đình; người chạy trail bán chuyên cần dịch vụ lẻ; doanh nghiệp đặt tour teambuilding.
- Vấn đề kinh doanh: (1) Thông tin cung đường (km, độ cao, độ khó) thiếu chuẩn hóa; (2) Thiếu linh hoạt khi tách lẻ gói dịch vụ và khó so sánh ngang hàng; (3) Bất tiện khi gom thông tin cá nhân, bảo hiểm, thuê đồ cho nhóm đông; (4) Đặt chỗ thủ công qua tin nhắn, thiếu cập nhật số chỗ trống (slot) thời gian thực, thanh toán online tự động và lưu vết hành trình.

3. Kết quả khảo sát ba website:
- Tổ Ong Adventure (https://toongadventure.com/): Mạnh về phân cấp độ khó (Level 1–4), tiêu chuẩn an toàn, lịch chọn ngày + slot trống và đặt online 4 bước; nhưng gói dịch vụ cố định, không có tài khoản lưu lịch sử hành trình, ưu đãi nhập thủ công.
- iTrek (https://itrek.vn/): Trải nghiệm cắm trại thân thiện người mới; nhưng thiếu chuẩn hóa độ khó, không có bộ lọc chuyên sâu, không hiện số slot, đặt tour và chuyển khoản cọc thủ công qua Zalo/Fanpage.
- Đi Chung Xe (https://www.dichungxe.net/): Đặt nhanh không cần đăng nhập (Guest Checkout), tách 2 hạng vé (trọn gói / tự túc); nhưng bị tách làm 2 web rời rạc, lịch khởi hành dạng ảnh khó lọc và không có tài khoản.

4. Danh sách yêu cầu do công cụ AI thứ nhất đề xuất:
- Vai trò: Guest, Member, Admin (gộp chung quản trị & điều hành). Vai trò HDV/Marketing/Đối tác phát triển sau.
- Chức năng bắt buộc (MVP): Phân loại danh mục; Tìm kiếm, lọc đa tiêu chí & So sánh 3 tour; Chi tiết tour & Lịch khởi hành kèm slot; Đăng ký/Đăng nhập, hồ sơ sức khỏe/liên hệ khẩn cấp & lưu vết hành trình (Trekking Passport); Đặt tour cho Guest & Member (chọn gói Trọn gói/Tự túc, thuê phụ kiện, nhập thông tin người đi cùng); Thanh toán Sandbox (VNPay/MoMo/QR) & cấp Booking Code; Tra cứu đơn bằng Mã đơn + SĐT; Admin CRUD tour, lịch khởi hành, slot, cập nhật trạng thái đơn và xuất danh sách khách.
- Chức năng phát triển sau / cần xác minh: Chia sẻ link đặt nhóm & chia tiền (Split Payment); Đánh giá xác thực sau chuyến đi; Tích điểm & ưu đãi khách cũ; Khóa chỗ tạm 15 phút (Slot Locking); Hoàn/hủy & dời lịch (Admin duyệt thủ công hay hoàn tiền tự động theo %).

Hãy phản biện các yêu cầu theo những khía cạnh:
- Có thực sự giải quyết vấn đề kinh doanh không?
- Có yêu cầu nào trùng lặp hoặc không cần thiết không?
- Có chức năng nào vượt quá phạm vi của nhóm không?
- Có thiếu chức năng cơ bản hoặc quy trình nghiệp vụ nào không?
- Có rủi ro về dữ liệu, bảo mật hoặc quyền riêng tư không?
- Có yêu cầu nào chưa đủ rõ để lập trình và kiểm thử không?
Với mỗi vấn đề, hãy nêu lý do và đề xuất điều chỉnh.
Không mặc định rằng phương án của công cụ AI trước là đúng.
Không tự ý thay đổi toàn bộ đề tài.
```

### Kết quả đề xuất

- **Vấn đề kinh doanh:** thang độ khó chưa có tiêu chí chấm; vấn đề 3 (gom thông tin nhóm đông) chưa được giải quyết vì link đặt nhóm bị để sau; chưa có chức năng cho khách doanh nghiệp; ưu đãi khách cũ nên làm sớm vì là điểm yếu của Tổ Ong và iTrek.
- **Trùng lặp, mâu thuẫn:** đề xuất ghi lúc VNPay/VietQR, lúc VNPay/MoMo/QR; xuất danh sách khách vừa bắt buộc vừa nâng cao; giữ chỗ 15 phút bị để sau dù là quy tắc lõi.
- **Vượt phạm vi:** chia tiền nhóm, hoàn tiền tự động theo %, nhiều cổng thanh toán, giỏ hàng nhiều tour, tách nhiều vai trò quản trị (dễ trễ tiến độ 12 tuần).
- **Còn thiếu:** xử lý trường hợp khách đã trả tiền mà hết chỗ; sơ đồ trạng thái đơn đầy đủ; email xác nhận; công thức tính giá; Admin hủy cả đợt; quên mật khẩu.
- **Dữ liệu, bảo mật:** thông tin sức khỏe là dữ liệu cá nhân nhạy cảm theo Luật Bảo vệ dữ liệu cá nhân 2025 (Nghị định 356/2025/NĐ-CP); cần ô đồng ý khi nhập thông tin người đi cùng; kiểm tra chữ ký kết quả thanh toán; mã đặt chỗ ngẫu nhiên.
- **Chưa rõ để kiểm thử:** "thời gian thực", ngưỡng độ khó, cách tính tổng km, tiêu chí nghiệm thu.

### Phản biện

Đây là lần phản biện cho kết quả của Lần sử dụng 1. Nhóm thảo luận từng ý trong buổi họp nhóm và không áp dụng tất cả (xem bảng dưới).

### Quyết định của nhóm

| Nội dung                         | Quyết định | Ghi chú                                                                |
| -------------------------------- | ---------- | ---------------------------------------------------------------------- |
| Tìm kiếm và lọc tour             | Giữ lại    | Chốt thang Dễ / Trung bình / Khó                                       |
| So sánh 3 tour                   | Loại bỏ    | Không cốt lõi, để dành thời gian cho phần chính                        |
| Đặt tour không cần đăng nhập     | Loại bỏ    | Nhóm chọn bắt buộc đăng nhập để lưu lịch sử tour                       |
| Lịch sử tour (Trekking Passport) | Giữ lại    |                                                                        |
| Hạng vé và thuê phụ kiện         | Giữ lại    | Bổ sung công thức tính giá                                             |
| Thanh toán trực tuyến            | Điều chỉnh | Chỉ dùng VNPay Sandbox, thanh toán đủ một lần                          |
| Giỏ hàng                         | Điều chỉnh | Nhóm giữ giỏ hàng nhưng chỉ gồm 1 tour và trang bị thuê kèm            |
| Giữ chỗ tạm 15 phút              | Điều chỉnh | Chuyển từ "phát triển sau" sang bắt buộc                               |
| Yêu cầu hủy / dời tour           | Giữ lại    | Nhân viên duyệt thủ công                                               |
| Hoàn tiền tự động theo %         | Loại bỏ    | Xử lý thủ công                                                         |
| Email xác nhận đơn               | Bổ sung    | Do AI thứ hai đề xuất                                                  |
| Ưu đãi khách cũ                  | Điều chỉnh | Làm bản đơn giản, 1 loại ưu đãi                                        |
| Đánh giá sau chuyến đi           | Để sau     | Mức "Nên có"                                                           |
| Chia tiền / link đặt nhóm        | Loại bỏ    | Vượt phạm vi                                                           |
| Hồ sơ thông tin sức khỏe         | Loại bỏ    | Thay bằng ô xác nhận đủ sức khỏe                                       |
| Form yêu cầu tour doanh nghiệp   | Bổ sung    | Dùng chung form gửi yêu cầu tư vấn                                     |
| Vai trò quản trị                 | Điều chỉnh | Nhóm không gộp 1 Admin mà tách Quản trị hệ thống và Điều hành / Tư vấn |
| Vai trò Marketing                | Giữ lại    | Mức "Nên có"                                                           |
| Vai trò Hướng dẫn viên / Đối tác | Để sau     |                                                                        |
| Xuất Excel danh sách khách       | Để sau     | Trước mắt chỉ xem danh sách                                            |

Kết quả cuối cùng được cập nhật vào [REQUIREMENTS.md](REQUIREMENTS.md).

## Nguyên tắc

Không đưa thông tin đăng nhập, API key, token, dữ liệu cá nhân hoặc tài liệu không được phép công khai vào công cụ AI hay repository công khai.
