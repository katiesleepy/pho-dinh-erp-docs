# Cập nhật giấy báo giá & giá mua

## Yêu cầu chung

> Thêm tính năng **cập nhật giá mua từ cập nhật báo giá**.

## Giải pháp — nút "Cập nhật giá mua"

Trên màn hình chung **Cập nhật giấy báo giá**, thêm nút **Cập nhật giá mua**. Người dùng check chọn các phiếu cập nhật giấy báo giá; chương trình tạo mặc định qua **danh mục Cập nhật giá mua**:

| Trường | Quy tắc gán |
|---|---|
| **Mã vật tư** | Mã vật tư đang báo giá |
| **Đơn vị tính** | Gán bằng **đơn vị tính nhà cung cấp** |
| **Ngày hiệu lực** | Gán theo ngày hiệu lực |
| **Mã nhà cung cấp** | Gán bằng mã NCC báo giá |
| **Mã ngoại tệ** | Gán bằng mã ngoại tệ báo giá |
| **Giá mua** | Gán bằng **giá chưa thuế** |
| **Trạng thái** | Mặc định **còn sử dụng** |

## Báo cáo theo dõi biến động giá

Ghi nhận trong họp 15/07/2026 và phụ lục yêu cầu:

| Báo cáo | Mô tả |
|---|---|
| **Biến động giá mua** | Báo cáo xoay theo ngày |
| **Dashboard biểu đồ đường** | Theo dõi biến động cập nhật giá mua và cập nhật báo giá |

## Dự báo đặt hàng

Thêm tính năng **dự báo đặt hàng** dựa trên 4 yếu tố:

1. **Tồn kho** hiện tại
2. **Nhu cầu đặt thêm**
3. **Lịch sử 3 tháng gần nhất** được điều chuyển
4. **Định mức sử dụng**

!!! note
    Yêu cầu này ghi nhận trong họp 15/07/2026, chưa có mô tả giải pháp chi tiết trong BRD Mua hàng.
