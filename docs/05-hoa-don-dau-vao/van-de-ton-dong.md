# Vấn đề tồn đọng giai đoạn dùng thử

Ghi nhận bởi **Quỳnh Anh** trong quá trình dùng thử phần mềm, sẽ tiếp tục bổ sung nếu phát hiện thêm.

## 7 vấn đề phát sinh khi triển khai sâu

| # | Nội dung | Người ghi nhận |
|:---:|---|---|
| 1 | Thiếu cột **Tiền phí** trên bảng kê / màn hình hóa đơn | Quỳnh Anh |
| 2 | Cột **Tiền thuế** và **Tổng tiền** có tách ra được theo từng mức thuế suất không (hóa đơn nhiều thuế suất)? | Quỳnh Anh |
| 3 | Cột **Mã thuế** và cột **Thuế suất** đang hiển thị **không giống nhau** (không khớp) | Quỳnh Anh |
| 4 | Cột **Tên sản phẩm** có cho thêm/sửa trực tiếp trên phần mềm được không? | Quỳnh Anh |
| 5 | **Tính chất hóa đơn** (Ngày tạo, Thông báo sai sót 04SS) chưa được cập nhật theo **thời gian mới nhất** | Quỳnh Anh |
| 6 | **Địa chỉ công ty / NCC bị đảo** | Quỳnh Anh |
| 7 | **Kết xuất chưa lọc được** theo ngày / tháng / năm | Quỳnh Anh |

## Nhóm theo bản chất vấn đề

=== ":material-bug: Lỗi dữ liệu"

    - Cột **Mã thuế** và **Thuế suất** không khớp *(#3)*
    - Cột **Thuế suất** bị **trống ở nhiều mặt hàng** trong Bảng kê chi tiết
    - **Địa chỉ công ty / NCC bị đảo** *(#6)*
    - **Tính chất hóa đơn / 04SS** cập nhật không kịp thời *(#5)*

=== ":material-plus-box: Thiếu chức năng"

    - Thiếu cột **Tiền phí** *(#1)*
    - Chưa **tách thuế theo từng mức thuế suất** *(#2)*
    - Chưa **sửa được tên sản phẩm** *(#4)*
    - Chưa **lọc kết xuất theo ngày/tháng/năm** *(#7 — trùng yêu cầu bổ sung #3)*

=== ":material-help-circle: Chờ Arito trả lời"

    - Lấy đủ dữ liệu hóa đơn từ **01/01/2026** được không? *(hiện chỉ có T1 và T6/2026)*
    - **1 link quản lý nhiều tài khoản web thuế** (9 MST con của 0308455031)
    - Cột **Trạng thái (Chờ duyệt)** trong HachToan dùng để làm gì?
    - Cột **Ngày tạo** trong HachToan lấy dữ liệu từ nguồn nào?

=== ":material-close-octagon: Xác nhận không làm được"

    - Cột **Nội dung TBSS 04SS** — không lấy được
    - Cột **Hóa đơn liên quan** — không lấy được
    - **In nhanh hàng loạt** từ phần mềm — phải in từng mẫu *(KH giữ nguyên yêu cầu)*
    - **Link hóa đơn cần mã xác thực** — không tự động mở được

## Điểm cần Arito rà soát (từ Recap 02/07/2026)

1. Rà soát lại phần **lưu hình ảnh / thông tin tra cứu** hóa đơn (link, mã tra cứu)
2. Kiểm tra lại cột **Thuế suất bị trống** ở nhiều mặt hàng trong Bảng kê chi tiết
3. Kiểm tra lại các cột được đánh dấu **"Thêm"** ở cuối bảng BKMV (chỉnh)
4. Xem lại phương án **hiển thị song song 2 tab** Hóa đơn NCC / Hóa đơn TCT
5. Xử lý yêu cầu **ưu tiên lấy hóa đơn từ Email dù đã lấy từ TCT trước đó**, hiển thị song song 2 bản
6. Bổ sung tính năng **chọn khoảng thời gian khi kết xuất**

Xem đầy đủ tại [Việc còn tồn](../08-hop-va-quyet-dinh/viec-con-ton.md).
