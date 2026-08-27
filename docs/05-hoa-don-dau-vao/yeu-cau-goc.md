# 26 yêu cầu gốc và phản hồi Arito

Nguồn: sheet **YCcũ** trong `Arito-PD (04.04.2025).xlsx`, tổng hợp lại ngày 02/07/2026.

## Nhóm A — Tài khoản, truy cập, chính sách

| # | Nội dung yêu cầu | Phản hồi / Trạng thái Arito |
|:---:|---|---|
| 1 | Dùng **1 link đăng nhập** cho nhiều MST chi nhánh (mỗi MST có TK web thuế riêng) | Phân quyền được; dùng chung 1 link bằng cách **chia đơn vị cơ sở** |
| 2 | **Email do Arito cấp**, Phổ Đình giữ tài khoản; chỉ dùng để nhận hóa đơn | Đúng — giữ tài khoản **trong thời gian thuê** (không vĩnh viễn) |
| 6 | Sản phẩm thuê hàng năm; phí gia hạn **1.000.000đ/năm** vẫn xem dữ liệu; xuất Excel/PDF để lưu trữ | Đúng — đã có chính sách |
| 19 | Nếu phát sinh không lấy đủ hóa đơn, Arito hỗ trợ **không tính phí** | Arito hỗ trợ đẩy vào và giải thích nguyên nhân |
| 20 | Thuế thay đổi cần update PM hoặc đổi PM, Arito tự chỉnh không tính phí | **Update miễn phí** |
| 24 | Dung lượng lưu trữ hóa đơn; xử lý email khi ngừng sử dụng PM | Dừng nhận email CC khi kết thúc; chi phí lưu trữ xem mục 6 |

## Nhóm B — Thu thập hóa đơn

| # | Nội dung yêu cầu | Phản hồi / Trạng thái Arito |
|:---:|---|---|
| 3 | Lấy hóa đơn từ **3 nguồn**: Email NCC (PDF+XML), TCT, tải lên XML; **ưu tiên email**, báo trùng | Lấy được từ 3 nguồn; TCT lấy định kỳ ~nửa tháng/tháng; **chưa có bộ lọc theo nguồn** |
| 15 | Hóa đơn NCC gửi dạng **file nén** | PM tự lấy dữ liệu được |
| 16 | Hóa đơn gửi từ **link**, tự nhấp vào có file XML & PDF để tải | PM tự lấy được — **chỉ khi link không yêu cầu mã tra cứu** |
| 17 | Link đăng nhập tải hóa đơn **định kỳ** (điện, nước, internet) | PM tự xử lý nếu link không cần mã; hoặc **import XML** / gửi qua email `dochoadon` |
| 18 | Hóa đơn gửi link **cần mã xác thực** để mở | :material-alert: **Không xử lý tự động được**; PM hỗ trợ lọc mail chưa đọc vào cụm để xử lý nhanh |
| 23 | Thời gian cập nhật hóa đơn từ NCC để kịp phát hiện sai trong kỳ kê khai | PM tự động cập nhật **sau khi thuế chấp nhận**; user có thể chủ động *Lấy hóa đơn* |
| 26 | Lấy được **toàn bộ** hóa đơn đầu vào và xử lý chính xác | Lấy được HĐ qua email; một số TH lỗi (sai thông tin, trùng, link cần mã) **KH tự tải & gửi qua email** |

## Nhóm C — Hiển thị, cảnh báo, theo dõi

| # | Nội dung yêu cầu | Phản hồi / Trạng thái Arito |
|:---:|---|---|
| 5 | Màn hình chính: thêm cột **trạng thái/lỗi hóa đơn** và cột **tên chi nhánh viết tắt** (hoặc MST) | Chỉnh sửa được — OK |
| 12 | **Cảnh báo** (chuông/tô màu) khi hóa đơn đã tải bị hủy/thay thế/điều chỉnh/04SS | Ghi nhận — Chỉnh sửa được (tô màu hoặc check) |
| 14 | Hóa đơn **đã xuất bảng kê**: tô màu dòng / nút check để nhận biết | Chỉnh sửa được |
| 21 | Phát hiện hóa đơn sai cần làm **04SS**: đưa sẵn thông tin cần chỉnh vào mẫu, phản hồi KH | Chỉnh sửa — thiết kế mẫu nhập/lưu thông tin điều chỉnh, **gửi email KH** |
| 22 | Tự thiết lập mẫu cần điều chỉnh lỗi sai về hóa đơn | Chỉnh sửa (xử lý nghiệp vụ hóa đơn bán) |

## Nhóm D — Kết xuất, in, lưu trữ

| # | Nội dung yêu cầu | Phản hồi / Trạng thái Arito |
|:---:|---|---|
| 4 | **In hàng loạt** theo chi nhánh, theo tháng/quý; in 2 mặt | :material-alert: **Không in nhanh từ PM**, phải in từng mẫu; **KH giữ nguyên yêu cầu in** |
| 7 | Kết xuất Excel **bảng kê mua vào**, lọc theo thời gian & chi nhánh, không giới hạn số HĐ | Chỉnh sửa được — thêm bộ lọc thời gian & chi nhánh |
| 8 | Kết xuất Excel **bảng hạch toán theo từng dòng** (tên hàng, SL, đơn giá, VAT, CK, giảm giá); dòng VAT cuối mỗi HĐ | Chỉnh sửa được |
| 9 | Chung 2 bảng (7 & 8): **số HĐ quy về 8 chữ số**; thêm cột tên chi nhánh viết tắt/MST người mua | Chỉnh sửa được |
| 10 | Tải **PDF & XML hàng loạt** theo MST; tên file theo cấu trúc `Tên NCC_Số hóa đơn` | Chỉnh sửa được |
| 11 | Xuất bảng kê mua vào: **chi tiết vật tư** và dạng **tổng hợp** | **Đã có** |

## Nhóm E — Hạch toán

| # | Nội dung yêu cầu | Phản hồi / Trạng thái Arito |
|:---:|---|---|
| 13 | Đẩy đủ dữ liệu nhập liệu từ PM hóa đơn sang **PM kế toán**; kết xuất hạch toán ra Excel | Chỉnh sửa được |
| 25 | Khi hạch toán, **tách Khuyến mãi (KM) và Chiết khấu (CK)** thành cột riêng | Chỉnh sửa — thêm cột KM, CK trên hóa đơn mua trong nước & dịch vụ |

---

## Hai điểm Arito không đáp ứng tự động

!!! danger "Cần xử lý thủ công"
    **#18 — Link cần mã xác thực:** phần mềm không mở được tự động. Giải pháp: PM lọc các mail chưa đọc vào một cụm để nhân viên xử lý nhanh bằng tay.

    **#4 — In nhanh hàng loạt:** phần mềm không in nhanh được, phải in từng mẫu. Khách hàng **giữ nguyên yêu cầu** — đây vẫn là điểm mở.
