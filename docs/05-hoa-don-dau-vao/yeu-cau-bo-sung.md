# 15 yêu cầu bổ sung (30/06/2026) và phản hồi 02/07/2026

Nguồn: sheet **YC** trong `3.Arito-PD (30.06.2025-gui Arito).xlsx`; phản hồi Arito ghi nhận trong buổi họp 02/07/2026.

| # | Nội dung yêu cầu | Phản hồi Arito (02/07/2026) |
|:---:|---|---|
| 1 | Thêm cột **Họ tên người mua hàng** tại Nhập liệu / Hóa đơn đầu vào | :material-check: **Thêm được — Đã có** |
| 2 | Thêm cột **Tệp đính kèm** *(xem Note6)* | :material-check: **Đã có** — hiển thị dạng **view bên trong** thay vì thêm cột riêng bên ngoài |
| 3 | Thêm lựa chọn **khoảng thời gian khi kết xuất** tại Nhập liệu / Hóa đơn đầu vào *(hiện đang kết xuất tất cả — Note7)* | :material-clock: **Ghi nhận, sẽ bổ sung sau** |
| 4 | Thêm & điều chỉnh **thứ tự các cột** trong file kết xuất tại Nhập liệu / Hóa đơn đầu vào *(chi tiết ở sheet BKMV (chỉnh))* | Cột **TBSS 04SS** và **Hóa đơn liên quan** :material-close: **không lấy được**; đổi tên cột P thành **"MST Đơn vị mua"**; bổ sung **chọn nhiều đơn vị** khi xuất Bảng kê hóa đơn |
| 5 | Thêm & điều chỉnh thứ tự cột trong file kết xuất tại Báo cáo / Bảng kê hóa đơn *(sheet HachToan (chỉnh))* | Xem chung phản hồi mục 4 |
| 6 | Cho phép **điều chỉnh chọn cột nào sẽ xuất ra** khi kết xuất *(Note3)* | — |
| 7 | Hóa đơn mua vào hiện chỉ có T1 và T6/2026 — có thể lấy đủ dữ liệu từ **01/01/2026** không? | :material-help: **Chờ Arito phản hồi** |
| 8 | **Tải file hóa đơn hàng loạt** để lưu trữ theo khoảng ngày | :material-check: **Xử lý được** |
| 9 | **1 link quản lý nhiều tài khoản web thuế** (MST con của MST mẹ 0308455031: -003, -005, -006, -007, -012, -013, -014, -016, -018). Đa số MST đã xuất hóa đơn về MST mẹ (~95%) | :material-help: **Chưa có phản hồi (đang chờ)** |
| 10 | Mở xem hóa đơn ở **2 tab song song**: Hóa đơn NCC và Hóa đơn TCT *(Note8)* | :material-eye: **Sẽ xem lại** (chưa xác nhận) |
| 11 | Mẫu hóa đơn Web Thuế trình bày **giống mẫu trên trang TCT** | :material-check: **Đã có** |
| 12 | Bổ sung bộ lọc phong phú hơn, ví dụ lọc **"hóa đơn rủi ro"** *(Note4)* | :material-check: **Đã có** |
| 13 | Có **nút check lại hóa đơn** để cập nhật trạng thái; có tự động check lại được không? *(Note5)* | :material-check: **Có** — chạy tự động **ban đêm**, quét lại hóa đơn **30 ngày gần nhất**, tự động cập nhật trạng thái |
| 14 | Xem chi tiết yêu cầu ghi trong comment của 2 sheet "BKMV (chỉnh)" và "HachToan (chỉnh)" | Xem [Mẫu kết xuất](bkmv-hach-toan.md) |
| 15 | Hóa đơn phải **ưu tiên lấy dữ liệu từ Email trước**, sau đó mới lấy từ Web Thuế | Ghi nhận (trùng với yêu cầu gốc #3) |

---

## Chi tiết yêu cầu #8 — Quy tắc đặt folder khi tải hàng loạt

=== "Tải theo tháng"

    - Mỗi NCC **1 folder**, đặt tên `MST_Tên NCC`
    - Nếu 1 hóa đơn có nhiều file (PDF, XML, file gửi email, file web thuế) → **gộp vào 1 folder**

=== "Tải theo năm"

    - Mỗi NCC **1 folder** `MST_Tên NCC`
    - Bên trong **chia theo tháng**: `T1`, `T2`, `T3`…

---

## Yêu cầu phát sinh thêm sau 30/06/2026

Ghi chú vận hành và các yêu cầu/lỗi mới phát sinh trong quá trình trao đổi tiếp theo:

| # | Nội dung | Trạng thái |
|:---:|---|---|
| 1 | Cơ chế kéo hóa đơn gồm 2 hình thức: **job tự động đầu ngày** và **kéo tay thủ công** | Đã có |
| 2 | Phần lưu **hình ảnh / thông tin tra cứu** (link, mã tra cứu) | :material-magnify: **Arito rà soát lại** |
| 3 | Hóa đơn **đã kê khai**: khi tải lại vẫn hiển thị nhưng hệ thống **không xóa** hóa đơn đã kê khai | Đã có (thiết kế hiện tại) |
| 4 | Bộ lọc khi kéo dữ liệu hóa đơn **đã tính luôn nguồn Email** (không chỉ TCT) | Đã có |
| 5 | Muốn **ưu tiên lấy hóa đơn từ Email dù trước đó đã lấy từ TCT**, đồng thời **hiển thị song song cả 2 bản** *(Note 4)* | :material-wrench: **Cần Arito xử lý** |
| 6 | Đổi tên trạng thái **"Hóa đơn gốc" → "Hóa đơn mới"** | Ghi nhận |
| 7 | Đổi nhãn màn hình lọc: **"Ngày từ/đến" → "Ngày hóa đơn"**; ô tick **"Tải lên từ TCT" → "Tải lên từ TCT, Email"** | Ghi nhận |
| 8 | **Mã NCC và Mã sản phẩm** cần tạo theo **1 định dạng thống nhất** | :material-account-group: **Cần thống nhất với khách hàng** |
| 9 | Một sản phẩm có **ĐVT chính và ĐVT quy đổi**, đồng thời **mua từ nhiều NCC** khác nhau | Ghi nhận, xử lý sau |
| 10 | Cột **Thuế suất** trong Bảng kê chi tiết đang **bị trống ở nhiều mặt hàng** | :material-bug: **Lỗi — Arito rà soát** |
| 11 | Kiểm tra lại các cột đánh dấu **"Thêm"** ở cuối bảng BKMV (chỉnh) | Cần rà soát lại |
| 12 | Cột **M (Thuế suất)** phải lấy đúng theo **từng dòng thuế suất** của hóa đơn; nhiều thuế suất thì hiển thị đầy đủ, **cách nhau bằng dấu phẩy** | Ghi nhận |

## Ghi chú kỹ thuật từ phụ lục (PHODINH PL THUẾ)

Các hạng mục Arito đã lên kế hoạch chỉnh sửa ở phía hệ thống:

| Menu | Nội dung chỉnh sửa |
|---|---|
| **Hóa đơn đầu vào** | Đọc thêm dữ liệu từ mail: lưu thêm **link tra cứu** và **mã tra cứu**. Đọc thêm dữ liệu `TTkhac`. Luôn ưu tiên Tổng cục Thuế |
| **Hóa đơn đầu vào** | Đổi tính chất hóa đơn *Hóa đơn gốc → Hóa đơn mới*. Thêm **Filter chung** để lọc trên grid (hiện chỉ lọc trên các cột grid). Thêm **tải hàng loạt**, tự gom theo NCC, lưu file XML + PDF |
| **Bảng kê hóa đơn** | Thêm mới một bảng kê (save as từ `inbkhd`): thêm cột từ bảng lưu hóa đơn, **tính lại ĐVT quy đổi**, tính lại **số lượng và giá**, ghép `0` cho **số hóa đơn đủ 8 số**, cho **sửa lưu số lượng và ĐVT trên grid báo cáo** |
| **Danh mục vật tư mapping** | Thêm mới — mỗi NCC một tên nên cần map lại theo mã danh mục vật tư, từ đó xác định **mã vật tư** và **ĐVT quy đổi** |

!!! warning "Mâu thuẫn cần làm rõ"
    Phụ lục kỹ thuật ghi *"Luôn ưu tiên tổng cục thuế"*, trong khi yêu cầu nghiệp vụ (#3 gốc, #15 bổ sung) là **ưu tiên Email trước**. Cần xác nhận lại thứ tự ưu tiên đúng với Arito.
