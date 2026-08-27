# Việc còn tồn & câu hỏi mở

Tổng hợp tất cả các điểm chưa chốt tính đến **27/08/2026**, gom từ BRD, meeting recap và bảng yêu cầu.

## :material-account-hard-hat: Arito chịu trách nhiệm

| # | Nội dung | Nguồn | Deadline |
|:---:|---|---|---|
| 1 | Rà soát phần lưu **hình ảnh / thông tin tra cứu** hóa đơn (link, mã tra cứu) | Recap 02/07 | Chưa xác định |
| 2 | :material-bug: Kiểm tra cột **Thuế suất bị trống** ở nhiều mặt hàng trong Bảng kê chi tiết | Recap 02/07 | Chưa xác định |
| 3 | Kiểm tra các cột đánh dấu **"Thêm"** ở cuối bảng BKMV (chỉnh) | Recap 02/07 | Chưa xác định |
| 4 | Xem lại phương án **hiển thị song song 2 tab** Hóa đơn NCC / TCT *(YC10)* | Recap 02/07 | Chưa xác định |
| 5 | Xử lý **ưu tiên lấy hóa đơn từ Email dù đã lấy từ TCT** trước đó, hiển thị song song 2 bản | Recap 02/07 | Chưa xác định |
| 6 | Bổ sung **chọn khoảng thời gian khi kết xuất** tại Nhập liệu / Hóa đơn đầu vào *(YC3)* | Recap 02/07 | Chưa xác định |
| 7 | Check lại **luồng xuất hóa đơn về tỉnh** giữa các chi nhánh | Recap 15/07 | Chưa xác định |
| 8 | Kiểm tra lại **nhà cung cấp kết nối** cho Phiếu xuất kho kiêm vận chuyển nội bộ | Recap 15/07 | Chưa xác định |

## :material-domain: Phổ Đình chịu trách nhiệm

| # | Nội dung | Nguồn |
|:---:|---|---|
| 1 | Cung cấp **người duyệt tương ứng của 3 cấp duyệt** phiếu nhu cầu vật tư | BRD Mua hàng |
| 2 | Gửi **danh sách hình thức thanh toán voucher** để thiết lập tài khoản khi đồng bộ POS | BRD TCKT |
| 3 | Xem lại **hạch toán 336 / 136** | Recap 15/07 |
| 4 | **Đồng nhất bộ mã** KH/NCC/vật tư giữa bản Quản trị và Tài chính trước khi chuyển dữ liệu | BRD TCKT |

## :material-account-group: Hai bên cùng thống nhất

| # | Nội dung | Nguồn |
|:---:|---|---|
| 1 | **Định dạng chuẩn cho Mã Nhà cung cấp và Mã sản phẩm** | Recap 02/07 |
| 2 | Luồng **điều chuyển thiết bị nội bộ** → mã của đơn vị mới xử lý thế nào | Recap 15/07 |
| 3 | Phương án **map giao dịch sổ phụ ngân hàng với giao dịch POS** | BRD TCKT — Quỹ |
| 4 | Quy tắc khớp mã **tài sản/công cụ đầu kỳ** giữa hai môi trường | Recap 15/07 |

## :material-help-circle: Câu hỏi chờ trả lời

| # | Câu hỏi | Chờ ai |
|:---:|---|---|
| 1 | Có thể lấy đủ dữ liệu hóa đơn từ **01/01/2026** không? *(hiện chỉ có T1 và T6/2026)* | Arito |
| 2 | **1 link quản lý nhiều tài khoản web thuế** cho 9 MST con của 0308455031? *(~95% MST đã xuất hóa đơn về MST mẹ)* | Arito |
| 3 | Cột **Trạng thái (Chờ duyệt)** trong HachToan dùng để làm gì? | Phổ Đình làm rõ |
| 4 | Cột **Ngày tạo** trong HachToan lấy dữ liệu từ nguồn nào? | Hai bên |
| 5 | Cột **Tiền thuế / Tổng tiền** tách được theo từng mức thuế suất không? | Arito |
| 6 | Cột **Tên sản phẩm** sửa trực tiếp trên phần mềm được không? | Arito |
| 7 | Thứ tự ưu tiên đúng: **Email trước** hay **TCT trước**? *(tài liệu mâu thuẫn)* | Arito |

## :material-close-octagon: Xác nhận không đáp ứng tự động

| Nội dung | Giải pháp thay thế |
|---|---|
| Cột **Nội dung TBSS 04SS** | Không lấy được — cần nhập thủ công hoặc bỏ |
| Cột **Hóa đơn liên quan** | Không lấy được — cần nhập thủ công hoặc bỏ |
| **In nhanh hàng loạt** từ phần mềm | Phải in từng mẫu. **KH giữ nguyên yêu cầu** — vẫn là điểm mở |
| **Link hóa đơn cần mã xác thực** | PM lọc mail chưa đọc vào cụm để xử lý thủ công nhanh |

## :material-clock-outline: Ghi nhận, xử lý sau

- Một sản phẩm có ĐVT chính + ĐVT quy đổi, mua từ nhiều NCC khác nhau
- Mở thêm **cột hình ảnh** trong phiếu yêu cầu
- Tiêu đề email bổ sung **nội dung diễn giải**
- Form in gửi NCC (bỏ phần ký nội bộ) và form in để lưu (có cấp duyệt)
- **Dự báo đặt hàng** (tồn kho, nhu cầu, lịch sử 3 tháng, định mức)
- Ba trường mới cho mẫu in m61: **Chức vụ**, **Thông số** (DMVT), **Tồn tức thời**
- **Phân loại quyền duyệt theo nhóm vật tư**
- Chi tiết chưa ghi nhận: giá vốn **chi nhánh nội thành** và **sản xuất**
