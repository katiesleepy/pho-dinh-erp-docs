# Template import danh mục

Bộ file Excel mẫu dùng để nhập liệu hàng loạt danh mục vào hệ thống Arito. Cột có dấu `*` là **bắt buộc**.

[:material-download: Tải toàn bộ template](../tai-lieu-goc.md#template-danh-muc){ .md-button }

---

## Danh mục Khách hàng / Nhà cung cấp

Hai file dùng **chung một cấu trúc 32 cột** — phân biệt bằng hai cột tick `Khách hàng` và `Nhà cung cấp`.

| # | Cột | | # | Cột |
|---|---|---|---|---|
| 1 | Mã khách hàng \* | | 17 | Nhóm 3 |
| 2 | Tên khách hàng \* | | 18 | Khu vực |
| 3 | Tên khác | | 19 | Điện thoại |
| 4 | Khách hàng | | 20 | Fax |
| 5 | Nhà cung cấp | | 21 | Thư (Email) |
| 6 | Địa chỉ | | 22 | Trang chủ (Website) |
| 7 | Mã số thuế | | 23 | Ghi chú |
| 8 | Người liên hệ | | 24 | Số tài khoản |
| 9 | Nhân viên bán hàng | | 25 | Tên ngân hàng |
| 10 | Tài khoản ngầm định | | 26 | Chi nhánh |
| 11 | Mã th.toán công nợ | | 27 | Tỉnh thành |
| 12 | Giới hạn tiền nợ | | 28 | Sử dụng hđ điện tử |
| 13 | Ngày sinh | | 29 | Loại khách hàng |
| 14 | Số CMND/CCCD | | 30 | Ph/th th.toán (HĐĐT) |
| 15 | Nhóm 1 | | 31 | Thư nhận HĐĐT |
| 16 | Nhóm 2 | | 32 | Người đại diện |

!!! tip
    `Mã khách hàng` phải theo quy tắc **10 ký tự**, đồng nhất giữa bản Quản trị và Tài chính — xem [Danh mục KH/NCC](khach-hang-ncc.md).

---

## Danh mục Vật tư, sản phẩm (37 cột)

**Định danh:** `Mã sản phẩm*` · `Tên sản phẩm*` · `Tên khác` · `Đơn vị tính*`

**Theo dõi:** `Theo dõi tồn kho` · `Theo dõi lô` · `Theo dõi tồn quy cách` · `Loại vật tư` · `Nhóm 1` · `Nhóm 2` · `Nhóm 3`

**Mặc định kho & thuế:** `Mã kho mặc định` · `Vị trí mặc định` · `Mã thuế mặc định` · `Mã thuế nhập khẩu`

**Tài khoản hạch toán:** `Tk kho/ chi phí` · `Sửa tk vật tư` · `Tk doanh thu` · `Tk giá vốn` · `Tk chiết khấu` · `Tk khuyến mãi` · `Tk trả lại` · `Tk s/p dở dang` · `Tk chi phí NVL`

**Thuộc tính:** `Mã phụ` · `Mã vạch (QRCode)` · `Thể tích` · `Khối lượng` · `Nước sản xuất` · `Màu sắc` · `Kích cỡ` · `Mã bộ phận`

**Định mức tồn:** `Tồn tối thiểu` · `Tồn tối đa` · `Ngày nhập cuối` · `Ngày xuất cuối` · `Ghi chú`

---

## Danh mục Đơn vị tính (4 cột)

`Đơn vị tính*` · `Tên đvt*` · `Tên khác` · `Đơn vị tính 2`

---

## Danh mục Quy đổi đơn vị tính (6 cột)

`Mã vật tư*` · `Tên vật tư` · `Đvt*` · `Hệ số*` · `Mã NCC*` · `Tên NCC`

!!! important "Hệ số quy đổi gắn theo NCC"
    Vì `Mã NCC` là trường bắt buộc, mỗi cặp (vật tư, ĐVT) có **hệ số quy đổi riêng theo từng nhà cung cấp**. Đây là nền tảng cho cột **Số lượng quy đổi** trong [bảng kê hạch toán](../05-hoa-don-dau-vao/bkmv-hach-toan.md).

---

## MAPPING.xlsx

File mapping tên vật tư: `Mã VT` ↔ `Tên VT Mapping`. Dùng để quy đổi tên vật tư do NCC ghi trên hóa đơn về mã vật tư nội bộ — xem [Danh mục vật tư mapping HĐĐV](../03-tckt/mua-hang-ke-toan.md#danh-muc-vat-tu-mapping-hv).
