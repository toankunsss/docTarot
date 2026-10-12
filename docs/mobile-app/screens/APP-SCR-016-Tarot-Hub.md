# APP-SCR-016 — Tarot Hub

| Thuộc tính | Giá trị |
|---|---|
| Screen ID | APP-SCR-016 |
| Module | APP-03 — Tarot |
| Route | `/tarot` |
| Phiên bản | 1.0 |
| Trạng thái | DRAFT — chi tiết hóa theo ảnh giao diện tham chiếu |

## 1. Tên và mục đích màn hình

- **Tên màn hình:** Bói Tarot.
- **Mục đích:** Là điểm vào chính của các trải nghiệm Tarot. Màn hình cho phép người dùng rút bài nhanh, xem lá bài của tháng, duyệt bộ sưu tập và chọn chủ đề trải bài.
- **Actor chính:** Người dùng Guest hoặc người dùng đã đăng nhập.
- **Điểm vào:** Nhấn tab “Bói Tarot”; nhấn lối tắt “Bói Bài” trên Home; quay lại từ một luồng Tarot; deep link hợp lệ.
- **Điểm ra:** Xáo và rút bài, chi tiết lá bài tháng, bộ sưu tập Tarot, chọn chủ đề trải bài, Profile, Home, Cung Sao và Paywall khi quyền sử dụng không đủ.

### Thành phần quan sát được từ ảnh

- Header có logo Aura Luna, mô tả thương hiệu, số dư Sao, avatar và chấm trạng thái.
- Hero card “Bốc Lá Bài Hôm Nay” có hình ba lá bài úp và CTA “Xáo Bài & Rút Lá Ngẫu Nhiên”.
- Card “Lá Bài Của Tháng” hiển thị The Moon, tên tiếng Việt “Mộng Tưởng”, câu diễn giải và CTA “Khám phá ý nghĩa”.
- “Bộ Sưu Tập Mộng Mơ” hiển thị tổng cộng tám lá và ba lá xem trước: The Fool, The Magician, High Priestess.
- “Chủ Đề Trải Bài” hiển thị bốn chủ đề: Tình Duyên, Sự Nghiệp, Chữa Lành và Có / Không; có nút “Xem tất cả (8)”.
- Bottom navigation trong ảnh hiển thị Trang Chủ, Bói Tarot và Cung Đạo/Cung Sao. Theo baseline sản phẩm trước đó có thêm tab “Tôi”; điểm khác biệt này cần xác nhận.

> **Lưu ý:** Chữ trong ảnh chỉ là nội dung tham khảo. Tên chính thức, hạn mức và nội dung diễn giải phải lấy từ cấu hình sản phẩm đã duyệt.

## 2. Chức năng tổng quan

- **Nhận biết tài khoản:** Hiển thị số dư Sao, avatar và trạng thái tài khoản.
- **Rút bài nhanh:** Cho phép xáo và rút một lá ngẫu nhiên từ hero card.
- **Lá bài của tháng:** Hiển thị lá đại diện trong tháng và mở diễn giải chi tiết.
- **Bộ sưu tập:** Cho phép xem các lá đã mở khóa/đã khám phá và truy cập toàn bộ bộ bài.
- **Chọn chủ đề:** Mở luồng trải bài theo Tình Duyên, Sự Nghiệp, Chữa Lành hoặc Có / Không.
- **Xem tất cả chủ đề:** Hiển thị đầy đủ danh sách tám chủ đề trải bài.
- **Điều hướng chính:** Chuyển giữa Trang Chủ, Bói Tarot, Cung Sao và Tôi theo cấu hình bottom navigation đã chốt.
- **Quyền Premium:** Người dùng Premium được rút/trải bài nhiều lần hơn; người dùng thường được giải thích hạn mức và chỉ mở Paywall sau thao tác chủ động.

## 3. Đặc tả thành phần giao diện

| STT | Thành phần | Loại | Bắt buộc | Chỉnh sửa | Dùng để làm gì | Khi thao tác | Kết quả hiển thị hoặc điều hướng |
|---|---|---|---|---|---|---|---|
| 1 | Logo “Aura Luna” | Logo/Button | Có | Không | Nhận diện thương hiệu | Nhấn | Cuộn màn lên đầu; không mở chồng Tarot Hub |
| 2 | Mô tả thương hiệu | Text | Có | Không | Thể hiện định vị ứng dụng | Không thao tác | Hiển thị nội dung cấu hình, ví dụ “Chữa lành & Chiêm tinh” |
| 3 | Số dư Sao | Badge/Button | Có | Không | Hiển thị số Sao hiện có | Nhấn | Mở bottom sheet giải thích số dư và cách sử dụng; chi tiết cần xác nhận |
| 4 | Avatar và chấm trạng thái | Avatar/Button | Có | Theo hồ sơ | Nhận biết tài khoản hiện hành | Nhấn | Mở APP-SCR-045 Profile |
| 5 | Hero “Bốc Lá Bài Hôm Nay” | Card | Có | Không | Giới thiệu hành động Tarot nhanh trong ngày | Nhấn card | Giống hành vi CTA rút bài |
| 6 | Nhãn “Năng lượng ngày mới” | Badge | Không | Không | Thể hiện ngữ cảnh nội dung theo ngày | Không thao tác | Không điều hướng |
| 7 | Ba lá bài úp | Illustration | Có | Không | Minh họa hành động xáo và rút bài | Nhấn | Bắt đầu CTA rút bài nếu card cho phép nhấn toàn vùng |
| 8 | CTA “Xáo Bài & Rút Lá Ngẫu Nhiên” | Button | Có | Không | Bắt đầu trải nghiệm rút nhanh | Nhấn | Còn lượt: mở APP-SCR-020; hết lượt: hiển thị thông tin hạn mức và CTA Premium |
| 9 | Card “Lá Bài Của Tháng” | Card | Có | Không | Tóm tắt lá bài đại diện trong tháng | Nhấn | Mở chi tiết lá bài tháng; màn đích cần xác nhận giữa APP-SCR-022 và màn Card Detail riêng |
| 10 | Ảnh lá bài tháng | Image/Button | Có | Không | Nhận diện lá bài | Nhấn | Giống hành vi card “Lá Bài Của Tháng” |
| 11 | Tên lá và tên diễn giải | Text | Có | Không | Hiển thị tên tiếng Anh và tiếng Việt | Không thao tác | Hiển thị nội dung đã được duyệt |
| 12 | Trích dẫn lá bài tháng | Text | Có | Không | Cung cấp thông điệp ngắn | Không thao tác | Tối đa số dòng theo thiết kế; không cắt mất ý nghĩa |
| 13 | “Khám phá ý nghĩa” | Text Button | Có | Không | Xem diễn giải đầy đủ | Nhấn | Mở chi tiết lá bài tháng |
| 14 | Tiêu đề “Bộ Sưu Tập Mộng Mơ” | Section title | Có | Không | Định danh khu vực bộ sưu tập | Không thao tác | Không điều hướng |
| 15 | Tổng số lá | Counter/Text Button | Có | Không | Hiển thị số lá đã có hoặc tổng số lá trong bộ sưu tập | Nhấn | Mở toàn bộ bộ sưu tập; ý nghĩa của số “8 lá bài” cần xác nhận |
| 16 | Danh sách lá xem trước | Horizontal list | Có | Không | Hiển thị ba hoặc nhiều lá nổi bật | Vuốt ngang | Xem thêm các lá nếu danh sách cho phép cuộn |
| 17 | Một lá trong bộ sưu tập | Card/Button | Có | Không | Xem tên và hình lá bài | Nhấn | Mở chi tiết đúng lá; màn đích cần xác nhận |
| 18 | Tiêu đề “Chủ Đề Trải Bài” | Section title | Có | Không | Định danh nhóm chủ đề | Không thao tác | Không điều hướng |
| 19 | “Xem tất cả (8)” | Text Button | Có | Không | Xem đầy đủ tám chủ đề | Nhấn | Mở APP-SCR-017 Tarot Topic Selection |
| 20 | Chủ đề “Tình Duyên” | Topic card | Có | Không | Bắt đầu trải bài tình cảm | Nhấn | Mở APP-SCR-018 với chủ đề Tình Duyên đã chọn; hoặc APP-SCR-017 nếu cần xác nhận lại |
| 21 | Badge “Hot” | Badge | Không | Không | Đánh dấu chủ đề nổi bật | Không thao tác | Không thay đổi quyền sử dụng |
| 22 | Chủ đề “Sự Nghiệp” | Topic card | Có | Không | Bắt đầu trải bài công việc | Nhấn | Mở APP-SCR-018 với chủ đề Sự Nghiệp đã chọn |
| 23 | Badge “Mới” | Badge | Không | Không | Đánh dấu chủ đề mới phát hành | Không thao tác | Không điều hướng |
| 24 | Chủ đề “Chữa Lành” | Topic card | Có | Không | Bắt đầu trải bài chữa lành | Nhấn | Mở APP-SCR-018 với chủ đề Chữa Lành đã chọn |
| 25 | Chủ đề “Có / Không” | Topic card | Có | Không | Bắt đầu trải bài một lá trả lời nhanh | Nhấn | Mở APP-SCR-019 hoặc APP-SCR-018 theo flow đã duyệt; cần xác nhận |
| 26 | Tab “Trang Chủ” | Bottom tab | Có | Không | Điều hướng về Home | Nhấn | Mở APP-SCR-011 Home |
| 27 | Tab “Bói Tarot” | Bottom tab | Có | Không | Xác định tab hiện tại | Nhấn lại | Cuộn lên đầu; không mở chồng Tarot Hub |
| 28 | Tab “Cung Sao” | Bottom tab | Có | Không | Điều hướng tới Zodiac | Nhấn | Premium: mở APP-SCR-024; thường: mở APP-SCR-053 sau thao tác chủ động |
| 29 | Tab “Tôi” | Bottom tab | Theo baseline | Không | Điều hướng tới Profile | Nhấn | Mở APP-SCR-045; cần xác nhận vì ảnh không hiển thị tab này |
| 30 | Pull-to-refresh | Gesture | Không | N/A | Làm mới nội dung Tarot Hub | Kéo xuống | Cập nhật hạn mức, lá tháng, bộ sưu tập và chủ đề; không thay lá đã cấp |

## 4. Use Case

### UC-TAROT-HUB-01 — Mở Tarot Hub

| Trường | Nội dung |
|---|---|
| Use Case ID | UC-TAROT-HUB-01 |
| Name | Xem trung tâm Tarot |
| Description | Hiển thị các hành động và nội dung Tarot chính |
| Actor | Guest hoặc người dùng đã đăng nhập |
| Preconditions | Đã hoàn tất onboarding và có phiên ứng dụng hợp lệ |
| Trigger | Nhấn tab “Bói Tarot” hoặc lối tắt “Bói Bài” |
| Main Flow | 1. Hệ thống hiển thị cấu trúc và skeleton theo khối. 2. Hệ thống tải số dư, quyền lợi, lá tháng, bộ sưu tập và chủ đề. 3. Từng khối hiển thị dữ liệu. 4. Người dùng chọn hành động mong muốn. |
| Alternative Flow | Nếu chưa có bộ sưu tập, hiển thị empty state và CTA bắt đầu rút bài. |
| Exception Rules | Lỗi một khối không khóa các khối khác. Lỗi toàn màn vẫn cho phép đổi tab. |
| Postconditions | Tarot Hub sẵn sàng cho thao tác hợp lệ. |

### UC-TAROT-HUB-02 — Rút lá ngẫu nhiên

| Trường | Nội dung |
|---|---|
| Use Case ID | UC-TAROT-HUB-02 |
| Name | Xáo bài và rút lá ngẫu nhiên |
| Description | Bắt đầu luồng rút bài nhanh từ hero |
| Actor | Người dùng |
| Preconditions | Hero tải thành công; trạng thái lượt sử dụng đã xác định |
| Trigger | Nhấn “Xáo Bài & Rút Lá Ngẫu Nhiên” |
| Main Flow | 1. Hệ thống kiểm tra lượt và quyền sử dụng. 2. Hệ thống khóa CTA để chống nhấn lặp. 3. Hệ thống mở APP-SCR-020. 4. Người dùng xáo, chọn và tiếp tục luồng reveal. |
| Alternative Flow | Người dùng Premium có hạn mức cao hơn và được tiếp tục nếu còn lượt. |
| Exception Rules | Hết lượt thì không bắt đầu rút; hiển thị hạn mức và CTA “Khám phá Premium”. Lỗi kiểm tra lượt cho phép Retry. |
| Postconditions | Luồng rút bài được tạo đúng một lần hoặc người dùng nhận được hướng dẫn tiếp theo. |

### UC-TAROT-HUB-03 — Xem lá bài của tháng

| Trường | Nội dung |
|---|---|
| Use Case ID | UC-TAROT-HUB-03 |
| Name | Xem diễn giải lá bài tháng |
| Description | Mở nội dung đầy đủ của lá đại diện trong tháng |
| Actor | Người dùng |
| Preconditions | Có lá tháng hợp lệ |
| Trigger | Nhấn card hoặc “Khám phá ý nghĩa” |
| Main Flow | 1. Hệ thống mở chi tiết đúng lá và đúng tháng. 2. Hệ thống hiển thị hình, tên và diễn giải. 3. Quay lại trở về đúng vị trí trên Tarot Hub. |
| Alternative Flow | Nếu nội dung chi tiết là Premium, hiển thị teaser và CTA Premium. |
| Exception Rules | Không tải được chi tiết thì hiển thị Retry; không thay đổi lá tháng. |
| Postconditions | Không thay đổi trạng thái hoặc lịch sử trải bài của người dùng. |

### UC-TAROT-HUB-04 — Xem một lá trong bộ sưu tập

| Trường | Nội dung |
|---|---|
| Use Case ID | UC-TAROT-HUB-04 |
| Name | Mở chi tiết lá sưu tập |
| Description | Xem hình và ý nghĩa của một lá Tarot |
| Actor | Người dùng |
| Preconditions | Lá tồn tại và có quyền xem |
| Trigger | Nhấn một card lá bài |
| Main Flow | 1. Hệ thống nhận diện lá được chọn. 2. Hệ thống mở chi tiết đúng lá. 3. Khi quay lại, giữ vị trí cuộn/danh sách. |
| Alternative Flow | Lá bị khóa hiển thị trạng thái khóa và điều kiện mở. |
| Exception Rules | Lá không còn khả dụng thì hiển thị thông báo và làm mới bộ sưu tập. |
| Postconditions | Bộ sưu tập không bị thay đổi nếu người dùng chỉ xem. |

### UC-TAROT-HUB-05 — Chọn chủ đề trải bài

| Trường | Nội dung |
|---|---|
| Use Case ID | UC-TAROT-HUB-05 |
| Name | Bắt đầu trải bài theo chủ đề |
| Description | Chọn chủ đề và tiếp tục sang cấu hình trải bài |
| Actor | Người dùng |
| Preconditions | Chủ đề đang hoạt động và người dùng đủ quyền |
| Trigger | Nhấn card chủ đề |
| Main Flow | 1. Hệ thống lưu chủ đề được chọn trong phiên. 2. Hệ thống mở APP-SCR-018 hoặc bước kế tiếp đã cấu hình. 3. Màn đích hiển thị đúng chủ đề. |
| Alternative Flow | Nhấn “Xem tất cả (8)” mở APP-SCR-017 để chọn từ danh sách đầy đủ. |
| Exception Rules | Chủ đề chưa phát hành hoặc bị khóa phải hiển thị lý do và hành động tiếp theo. |
| Postconditions | Chủ đề được truyền đúng vào luồng trải bài. |

## 5. Business Rules

### BR1. Hạn mức Tarot

- Người dùng thường và Premium có hạn mức khác nhau.
- Premium được rút/trải bài nhiều lần hơn.
- Hạn mức cụ thể theo ngày hoặc theo kỳ là `Cần xác nhận`.
- Khi hết lượt, không tự động trừ Sao hoặc mở Paywall.

### BR2. Chống cấp kết quả trùng

- Một thao tác nhấn chỉ tạo một phiên rút bài.
- Retry do lỗi mạng không được tạo thêm phiên hoặc cấp thêm lá ngoài ý muốn.

### BR3. Lá bài của tháng

- Mỗi người dùng có tối đa một lá đại diện cho một tháng nếu nghiệp vụ dùng kết quả cá nhân hóa.
- Refresh không thay đổi lá tháng.
- Khi sang tháng mới, hệ thống hiển thị nội dung của tháng mới theo quy tắc đã duyệt.

### BR4. Bộ sưu tập

- Chỉ hiển thị lá mà người dùng được phép xem.
- Thứ tự hiển thị trong ảnh là theo số thứ tự Major Arcana; quy tắc sắp xếp chính thức cần xác nhận.
- Bộ đếm phải làm rõ là số lá đã sở hữu, đã khám phá hay tổng số lá; không dùng nhãn mơ hồ.

### BR5. Chủ đề trải bài

- Chủ đề hiển thị theo cấu hình đang hoạt động.
- Badge “Hot” và “Mới” chỉ là nhãn nội dung, không thay đổi quyền.
- “Có / Không” phải được mô tả là gợi ý tham khảo, không phải dự đoán chắc chắn.

### BR6. Nội dung an toàn

- Không khẳng định chắc chắn về y tế, pháp lý, tài chính, sự sống hoặc định mệnh.
- Khi câu hỏi thuộc phạm vi nhạy cảm, luồng sau phải hướng người dùng tới cách diễn đạt an toàn.

### BR7. Premium

- Nội dung khóa phải có badge hoặc trạng thái khóa rõ.
- Chỉ mở APP-SCR-053 khi người dùng chủ động nhấn nội dung bị khóa hoặc CTA Premium.
- Đóng Paywall phải quay về đúng vị trí trên Tarot Hub.

### BR8. Giữ ngữ cảnh

- Khi quay lại từ màn chi tiết, Tarot Hub giữ vị trí cuộn.
- Chủ đề đang chọn được giữ trong luồng nhưng phải xóa khi người dùng hủy toàn bộ trải bài.

## 6. Validation

| Trường hoặc hành động | Điều kiện hợp lệ | Điều kiện không hợp lệ | Thông báo hiển thị |
|---|---|---|---|
| Rút lá ngẫu nhiên | Còn lượt và trạng thái quyền đã xác định | Hết lượt | “Bạn đã dùng hết lượt trải bài hiện tại.” |
| Kiểm tra lượt | Tải được hạn mức hiện tại | Không thể xác định | “Không thể kiểm tra lượt trải bài. Vui lòng thử lại.” |
| Mở lá tháng | Có lá và nội dung hợp lệ | Chưa có hoặc không tải được | “Chưa thể hiển thị lá bài của tháng. Vui lòng thử lại.” |
| Mở lá trong bộ sưu tập | Lá tồn tại và có quyền xem | Lá bị khóa hoặc không tồn tại | “Lá bài này chưa được mở khóa.” hoặc “Không tìm thấy lá bài.” |
| Chọn chủ đề | Chủ đề đang hoạt động | Chủ đề chưa phát hành hoặc bị khóa | “Chủ đề này hiện chưa khả dụng.” |
| Nhấn CTA liên tục | Chưa có thao tác đang xử lý | Đang loading | Không tạo request mới; giữ CTA ở trạng thái loading |
| Làm mới | Có mạng hoặc cache hợp lệ | Mất mạng và không có cache | “Không thể cập nhật Tarot. Vui lòng kiểm tra kết nối.” |

## 7. Trạng thái màn hình

| Trạng thái | Nội dung hiển thị | Thành phần được thao tác | Hành động tiếp theo |
|---|---|---|---|
| Loading lần đầu | Header, bottom navigation và skeleton theo khối | Đổi tab; mở Profile nếu phiên sẵn sàng | Chờ dữ liệu |
| Có dữ liệu | Hero, lá tháng, bộ sưu tập và chủ đề | Tất cả hành động hợp lệ | Chọn chức năng |
| Còn lượt | CTA rút bài ở trạng thái enabled | Rút bài | Mở APP-SCR-020 |
| Hết lượt | Hiển thị hạn mức và CTA Premium | Xem Premium hoặc quay lại | APP-SCR-053 khi chủ động nhấn |
| Bộ sưu tập rỗng | Thông điệp chưa có lá và CTA bắt đầu | Rút bài | Mở APP-SCR-020 hoặc APP-SCR-017 |
| Lá tháng chưa có | Placeholder và lời giải thích | Retry nếu phù hợp | Tải lại hoặc chờ điều kiện nghiệp vụ |
| Lỗi một phần | Khối lỗi có Retry; khối khác giữ dữ liệu | Retry riêng hoặc dùng khối khác | Tải lại khối |
| Lỗi toàn màn | Header, bottom navigation, thông báo và Retry | Retry hoặc đổi tab | Tải lại Tarot Hub |
| Offline có cache | Banner offline và dữ liệu gần nhất | Xem cache; không bắt đầu hành động cần mạng | Kết nối lại |
| Không đủ quyền | Teaser/badge Premium | Mở thông tin Premium | APP-SCR-053 |

## 8. Thông báo

| Mã | Trường hợp | Nội dung thông báo | Kiểu hiển thị | Thời điểm đóng |
|---|---|---|---|---|
| TAROT-HUB-M01 | Hết lượt | “Bạn đã dùng hết lượt trải bài hiện tại.” | Bottom sheet | Khi đóng hoặc chọn Premium |
| TAROT-HUB-M02 | Không kiểm tra được lượt | “Không thể kiểm tra lượt trải bài. Vui lòng thử lại.” | Inline + Retry | Khi Retry thành công |
| TAROT-HUB-M03 | Lỗi một khối | “Không thể tải nội dung. Vui lòng thử lại.” | Inline + Retry | Khi tải thành công |
| TAROT-HUB-M04 | Mất mạng | “Bạn đang ngoại tuyến. Một số nội dung có thể chưa được cập nhật.” | Banner | Khi có mạng lại |
| TAROT-HUB-M05 | Chủ đề chưa khả dụng | “Chủ đề này hiện chưa khả dụng.” | Toast/Snackbar | Tự đóng theo thời gian chuẩn |
| TAROT-HUB-M06 | Lá bị khóa | “Lá bài này chưa được mở khóa.” | Bottom sheet hoặc inline | Khi đóng hoặc thực hiện CTA |

## 9. Hiệu ứng và phản hồi

- Card và CTA có trạng thái nhấn rõ; không làm bố cục nhảy.
- Khi nhấn CTA rút bài, nút chuyển loading và khóa cho tới khi điều hướng hoặc báo lỗi.
- Animation xáo bài chỉ bắt đầu tại APP-SCR-020; Tarot Hub có thể dùng chuyển động nhẹ cho illustration nhưng không mô phỏng đã rút bài.
- Danh sách bộ sưu tập vuốt ngang phải dừng đúng card và không cản thao tác cuộn dọc.
- Bottom sheet hạn mức/Premium trượt từ dưới lên, nền phía sau tối nhẹ.
- Khi Reduce Motion bật, loại bỏ chuyển động bay/xáo trang trí và dùng đổi opacity ngắn.
- Lỗi một phần chỉ thay nội dung của khối lỗi; không làm các khối khác dịch chuyển bất thường.

## 10. Điều hướng

| Hành động | Điều kiện | Màn hình hoặc trạng thái đích | Dữ liệu cần giữ |
|---|---|---|---|
| Nhấn avatar | Luôn khả dụng | APP-SCR-045 Profile | Vị trí cuộn Tarot Hub |
| Nhấn CTA rút bài | Còn lượt | APP-SCR-020 Shuffle and Card Selection | Nguồn mở, loại rút nhanh, lượt đã giữ chỗ nếu có |
| Nhấn CTA rút bài | Hết lượt | Bottom sheet hạn mức | Vị trí Home và quyền lợi hiện tại |
| Nhấn CTA Premium | Không đủ lượt/quyền | APP-SCR-053 Premium Paywall | Màn nguồn và nội dung bị khóa |
| Nhấn lá bài tháng | Có dữ liệu | Màn chi tiết lá; `Cần xác nhận` Screen ID | Lá và tháng hiện tại |
| Nhấn một lá sưu tập | Có quyền | Màn chi tiết lá; `Cần xác nhận` Screen ID | ID lá và vị trí danh sách |
| Nhấn “Xem tất cả (8)” | Luôn khả dụng | APP-SCR-017 Tarot Topic Selection | Không |
| Nhấn “Tình Duyên” | Chủ đề hoạt động | APP-SCR-018 hoặc APP-SCR-017 | Chủ đề Tình Duyên |
| Nhấn “Sự Nghiệp” | Chủ đề hoạt động | APP-SCR-018 | Chủ đề Sự Nghiệp |
| Nhấn “Chữa Lành” | Chủ đề hoạt động | APP-SCR-018 | Chủ đề Chữa Lành |
| Nhấn “Có / Không” | Chủ đề hoạt động | APP-SCR-018 hoặc APP-SCR-019 | Chủ đề Có / Không |
| Nhấn tab “Trang Chủ” | Luôn khả dụng | APP-SCR-011 Home | Không |
| Nhấn tab “Bói Tarot” | Đang ở Tarot Hub | Cuộn lên đầu | Không |
| Nhấn tab “Cung Sao” | Có Premium | APP-SCR-024 Zodiac List | Không |
| Nhấn tab “Cung Sao” | Không có Premium | APP-SCR-053 | Màn nguồn |
| Nhấn tab “Tôi” | Tab được chốt hiển thị | APP-SCR-045 Profile | Không |

## 11. Tiêu chí nghiệm thu

- Khi người dùng mở Tarot Hub, hệ thống hiển thị header, hero rút bài, lá bài tháng, bộ sưu tập, chủ đề và bottom navigation đúng thứ tự.
- Khi người dùng còn lượt và nhấn “Xáo Bài & Rút Lá Ngẫu Nhiên”, hệ thống chỉ tạo một luồng và mở APP-SCR-020.
- Khi người dùng hết lượt, hệ thống không bắt đầu trải bài, hiển thị hạn mức và chỉ mở APP-SCR-053 sau khi người dùng nhấn CTA Premium.
- Khi người dùng nhấn liên tục CTA rút bài, hệ thống chỉ xử lý một lần.
- Khi lá bài tháng tải thành công, card hiển thị đúng ảnh, tên, tháng và thông điệp.
- Khi người dùng refresh, lá bài tháng và kết quả đã cấp không bị thay đổi ngoài quy tắc nghiệp vụ.
- Khi nhấn một lá trong bộ sưu tập, hệ thống mở đúng lá và giữ vị trí danh sách khi quay lại.
- Khi bộ sưu tập rỗng, hệ thống hiển thị giải thích và CTA bắt đầu rút bài; không hiển thị vùng trống.
- Khi nhấn “Xem tất cả (8)”, hệ thống mở APP-SCR-017 với đầy đủ chủ đề đang hoạt động.
- Khi nhấn một chủ đề, màn kế tiếp nhận đúng chủ đề đã chọn.
- Khi một khối tải lỗi, các khối còn lại và bottom navigation vẫn hoạt động; khối lỗi có Retry riêng.
- Khi mất mạng và có cache, hệ thống hiển thị dữ liệu gần nhất và banner offline; không giả vờ rút bài thành công.
- Khi dùng screen reader, mỗi lá được đọc bằng số thứ tự, tên tiếng Anh, tên tiếng Việt và trạng thái khóa nếu có.
- Khi tăng cỡ chữ, card chủ đề tăng chiều cao và không cắt mô tả.
- Khi Reduce Motion bật, giao diện không dùng animation xáo/bay trang trí trên Tarot Hub.

## Điểm cần xác nhận

1. Bottom navigation chính thức có ba tab như ảnh hay bốn tab như baseline gồm thêm “Tôi”.
2. Số “8 lá bài” là số lá đã sở hữu, đã khám phá hay tổng số lá của bộ sưu tập đang hiển thị.
3. Screen ID cho màn chi tiết một lá Tarot và chi tiết “Lá Bài Của Tháng”.
4. Khi nhấn trực tiếp card chủ đề, hệ thống mở APP-SCR-017 để xác nhận hay bỏ qua và mở APP-SCR-018.
5. Chủ đề “Có / Không” có cần qua chọn spread hay mở thẳng màn nhập câu hỏi.
6. Hạn mức cụ thể của người dùng thường và Premium; hạn mức theo ngày hay theo kỳ.
7. Sao được sử dụng cho giao dịch nào và nhấn số dư mở bottom sheet hay một màn lịch sử riêng.
8. Badge “Hot” và “Mới” được quản trị theo thời gian hay cấu hình thủ công.
