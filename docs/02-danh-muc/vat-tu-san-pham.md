# Danh mục vật tư, sản phẩm

## Bổ sung trường thông tin

Theo yêu cầu phân hệ Mua hàng, **Thông tin chung** của danh mục vật tư thêm:

| Trường mới | Mô tả |
|---|---|
| **Mã hàng NCC** | Nhập mã theo quy cách của nhà cung cấp |
| **Tên hàng NCC** | Nhập tên vật tư theo quy cách của nhà cung cấp |
| **Thông số** | Trường mới, dùng cho mẫu in Balet (m61_02) |

## Tab "Vật tư thay thế"

Thêm tab **Vật tư thay thế** vào danh mục vật tư, gồm:

- **Mã vật tư** — chọn từ danh mục vật tư
- **Tên vật tư** — mặc định hiện theo mã vật tư
- **Đơn vị tính** — mặc định hiện theo mã vật tư

Mục đích: khi NCC báo hết hàng, người dùng tra cứu nhanh ngay tại tab này các vật tư có thể thay thế. Đây là đầu vào cho tính năng **Truy vấn vật tư thay thế** ở [Phiếu phát triển sản phẩm R&D – NXU](../04-mua-hang/rd-nxu.md).

## Đơn vị tính và quy đổi

- Một sản phẩm có **đơn vị tính chính** và **đơn vị tính quy đổi**, đồng thời được **mua từ nhiều NCC khác nhau** — ghi nhận trong họp 02/07/2026, xử lý sau.
- Danh mục quy đổi đơn vị tính khai theo bộ: `Mã vật tư · Tên vật tư · ĐVT · Hệ số · Mã NCC · Tên NCC` — nghĩa là **hệ số quy đổi gắn theo từng nhà cung cấp**.
- Trong bảng kê hạch toán, các ĐVT **không có trong danh mục quy đổi thì giữ nguyên** khi chuyển sang cột ĐVT quy đổi.

## Các trường phục vụ hạch toán tự động

Danh mục vật tư khai báo các tài khoản để hệ thống áp bút toán:

| Trường | Dùng cho |
|---|---|
| Tk kho / chi phí | Nợ khi nhập kho |
| Tk doanh thu, Tk giá vốn | Bán hàng |
| Tk chiết khấu, Tk khuyến mãi, Tk trả lại | Các khoản giảm trừ |
| **Tk s/p dở dang** | Bút toán kết chuyển chi phí sản xuất (đầu 6 → 154) |
| Tk chi phí NVL | Giá thành |
| Mã thuế mặc định | Lấy lên cột VAT ở mẫu in m61_02 |
| Kích cỡ | Lấy lên cột Thông số ở mẫu in m61_02 |

Xem thêm: [Template import danh mục](template-import.md) · [Mẫu in m61](../07-bieu-mau-in/m61.md)
