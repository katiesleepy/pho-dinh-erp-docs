# Đơn đặt hàng

## Yêu cầu chung

- **Gửi mail cho NCC** sau khi duyệt đơn hàng.
- Khi vật tư không đủ, NCC báo tình trạng hàng → kho note thông tin và **tự sinh phiếu phát triển sản phẩm R&D**.

## Giải pháp thực hiện

### Nút gửi mail

Trên màn hình chung của Đơn đặt hàng, thêm **nút gửi mail** — bấm vào chương trình gửi mail đến nhà cung cấp theo **mẫu của Phổ Đình**.

### Kế thừa phiếu nhu cầu

- Sau khi phiếu nhu cầu vật tư được phê duyệt, bộ phận mua hàng **kế thừa các phiếu nhu cầu đã được phê duyệt**.
- **Điền lại mã vật tư chưa được tạo trước đó**, để các quy trình sau được kế thừa dữ liệu.

!!! tip "Đây là điểm khớp nối quan trọng"
    Ở ST1, vật tư chưa có mã được đặt bằng **mã vật tư chung**. Đến bước tạo đơn hàng, bộ phận mua hàng phải **điền lại mã vật tư thật** — nếu bỏ qua, các bước sau (hóa đơn, nhập kho, giá thành) sẽ không kế thừa được dữ liệu.

### Báo cáo tình trạng đơn hàng mua

Đơn đặt hàng có biến động → bộ phận kho vào **Báo cáo tình trạng đơn hàng mua** để ghi chú lại thông tin.

Chương trình **gán các thông tin mặc định** để tạo phiếu phát triển sản phẩm:

| Trường | Quy tắc gán mặc định |
|---|---|
| **Ngày cập nhật** | Theo ngày cập nhật thông tin cho bộ phận R&D |
| **Phân loại** | Loại vật tư là *nguyên liệu* → gán **Nguyên vật liệu**; loại *công cụ* → gán **Công cụ** |
| **Số phiếu** | Tự nhảy theo nguyên tắc **Mã đơn vị chi nhánh + YY + MM + 3 số tự nhiên** |
| **Mã hàng** | Theo mã vật tư cần xử lý |
| **Tên hàng, Đơn vị tính** | Tự load theo mã vật tư |
| **ĐVT order** | Theo đơn vị tính trên **đơn hàng mua** |
| **Nhà cung cấp** | Theo nhà cung cấp trên **đơn hàng** |
| **Lý do yêu cầu xử lý** | Kho chọn: *hết hàng / hủy / đổi mẫu / lý do khác* |

## Biểu mẫu

### Mẫu mail gửi nhà cung cấp

**Tiêu đề:** `Đơn đặt mua hàng công ty Phổ Đình`

**Nội dung:**

> **Đơn đặt hàng nhà cung cấp**
>
> - Phổ Đình đặt hàng ngày: *Ngày đơn hàng*
> - Ngày giao: *Lấy dữ liệu ngày giao hàng*
> - Nơi nhận: *Lấy từ nơi nhận*
> - Ghi chú giao hàng: *Lấy từ ghi chú giao hàng*
>
> | STT | Mã hàng | Tên hàng | Đơn vị tính | Số lượng |
> |---|---|---|---|---|

### Mẫu in đơn đặt hàng

Có mẫu in riêng (Hình 5 trong BRD Mua hàng) — xem [file gốc](../tai-lieu-goc.md).
