# Phiếu nhu cầu vật tư (m61)

## Yêu cầu chung

> Phiếu nhu cầu vật tư: cho thêm tính năng **truy vấn lại đơn hàng gần nhất** các nhà cung cấp nào.

## Nút "Kiểm tra lịch sử đặt hàng"

Thanh công cụ chi tiết màn hình phiếu nhu cầu thêm nút **Kiểm tra lịch sử đặt hàng**:

- Truy vấn dữ liệu **đơn hàng mua trong nước / nhập khẩu** trong **ba tháng gần nhất**.
- Cho **chọn lại thời gian ngày từ – đến** để lọc dữ liệu.
- Lọc theo **mã vật tư** có nhu cầu mua.

### Thông tin trả về

| Trường | Mô tả |
|---|---|
| Mã nhà cung cấp | Mã NCC có phát sinh đặt hàng |
| Tên nhà cung cấp | Tên NCC đặt hàng |
| Ngoại tệ | Ngoại tệ đặt hàng lần trước |
| Mã vật tư | Mã vật tư đặt hàng |
| Tên vật tư | Tên vật tư đặt hàng |
| Số lượng | Số lượng đặt hàng các lần trước |
| Đơn giá nguyên tệ | Đơn giá ngoại tệ đặt lần trước |
| Đơn giá VND | Đơn giá VND đặt lần trước |
| Thành tiền nguyên tệ | Giá trị đặt hàng bằng ngoại tệ |
| Thành tiền VND | Giá trị đặt hàng VND |

## Cấp duyệt

Set theo **3 cấp duyệt** của Phổ Đình.

!!! warning "Chờ Phổ Đình"
    Phổ Đình cung cấp sau **người duyệt tương ứng của mỗi cấp**. Ngoài ra phụ lục yêu cầu còn ghi: **thêm phân loại quyền duyệt theo nhóm vật tư**.

## Biểu mẫu in

Mẫu in phiếu nhu cầu vật tư (**m61**) có 2 biến thể: **Shunta (m61_01)** và **BALET (m61_02)**. Xem chi tiết ánh xạ từng cột tại [Mẫu in m61](../07-bieu-mau-in/m61.md).

## Yêu cầu bổ sung từ phản hồi khách hàng

Ghi nhận trong tài liệu HDSD Duyệt yêu cầu (phần phản hồi):

| # | Nội dung | Trạng thái |
|---|---|---|
| 1 | Mở thêm **cột hình ảnh** trong phiếu yêu cầu | Yêu cầu |
| 2 | Sản phẩm order mới **chưa có mã**, hoặc không nằm trong danh mục kho — có tạo được phiếu không? | **Câu hỏi chờ trả lời** — BRD trả lời: dùng **mã vật tư chung** + ghi chú tên thực tế + đính kèm hình |
| 3 | Tiêu đề email bổ sung thêm **nội dung diễn giải** để dễ nhận diện phiếu yêu cầu | Yêu cầu |
| 4 | **Form in để gửi NCC**: bỏ phần ký xác nhận các cấp nội bộ. Có cách nào liên kết email NCC chỉ cần nhấn nút là gửi luôn? | BRD trả lời: **có** — nút gửi mail trên [Đơn đặt hàng](don-dat-hang.md) |
| 5 | **Form in để lưu**: đầy đủ thông tin, có thể hiện thông tin cấp duyệt bên dưới phiếu | Yêu cầu |
| 6 | NCC báo hết hàng/không đủ số lượng → bổ sung cột **"hết hàng"** có link gắn email gửi đến bộ phận nội bộ khác xử lý tiếp | BRD trả lời bằng luồng **Báo cáo tình trạng đơn hàng mua → Phiếu R&D–NXU** |
