# Chuyển dữ liệu Quản trị → Tài chính

Đây là cơ chế xương sống của toàn hệ thống. Nắm được bảng "chuyển / không chuyển" bên dưới là nắm được phần lớn thiết kế.

## Quy trình 3 bước

| Bước | Người thực hiện | Đầu vào → Thực hiện → Đầu ra |
|---|---|---|
| **ST1. Nhập dữ liệu kế toán** | Kế toán | **Vào:** các danh mục dùng chung, chứng từ kế toán, hóa đơn mua hàng/mua dịch vụ/bán hàng…<br>**Làm:** khởi tạo danh mục dùng chung, nhập dữ liệu, **tick chọn** các chứng từ được phép chuyển sang Tài chính.<br>**Ra:** danh mục + chứng từ trên hệ thống Quản trị. |
| **ST2. Chuyển dữ liệu** | Kế toán | **Vào:** danh mục + chứng từ trên Quản trị.<br>**Làm:** vào **Hệ thống / Bảo trì số liệu / Chuyển số dư sang năm sau** để chạy chuyển từ Quản trị sang Tài chính.<br>**Ra:** danh mục, chứng từ đã sang Tài chính. |
| **ST3. Dữ liệu kế toán** | Kế toán | **Vào:** dữ liệu đã chuyển.<br>**Làm:** kiểm tra thông tin được chuyển, điều chỉnh nếu cần.<br>**Ra:** dữ liệu kế toán trên hệ thống Tài chính. |

## Danh mục được chuyển (toàn bộ)

- Danh mục khách hàng / nhà cung cấp
- Danh mục tài khoản
- Danh mục vật tư, sản phẩm
- Danh mục đơn vị tính
- Danh mục đơn vị tính quy đổi
- Danh mục tài sản
- Danh mục công cụ (hoặc chi phí trả trước)
- Danh mục thiết bị

## Chứng từ: chuyển hay không chuyển

| Chứng từ | Chuyển? | Ghi chú |
|---|:---:|---|
| Hóa đơn mua hàng **trong nước** | :material-close-circle:{ .no } Không | |
| Hóa đơn **mua dịch vụ** | :material-close-circle:{ .no } Không | |
| Hóa đơn mua **tài sản/công cụ nhập kho** | :material-check-circle:{ .yes } Có | Thêm trường **ngày hóa đơn gốc** để xác định kỳ kê khai gốc |
| Hóa đơn mua hàng **nhập khẩu** | :material-check-circle:{ .yes } Có | Chi phí kèm theo **không hợp lệ thì không chuyển** |
| Phiếu xuất điều chuyển | :material-close-circle:{ .no } Không | **Ngoại trừ** loại *Điều chuyển thiết bị* |
| Phiếu thanh toán tạm ứng | :material-check-circle:{ .yes } Có | |
| Bút toán điều chỉnh giảm công nợ | :material-check-circle:{ .yes } Có | |
| Chứng từ bù trừ công nợ | :material-check-circle:{ .yes } Có | |
| Các chứng từ khác phân hệ TCKT | :material-check-circle:{ .yes } Có | Nếu có tick vào ô **Chuyển dữ liệu** |

## Cách vận hành

- Với chứng từ cần chuyển, người dùng **chủ động check vào ô "Chuyển dữ liệu"**; chương trình sẽ chạy chuyển tất cả sang Tài chính.
- Tại màn hình **hóa đơn mua hàng nhập khẩu**, tab **Chi phí** thêm ô check **Chuyển dữ liệu**. Khi chuyển sang Tài chính, chương trình **không chuyển các dòng không check** và **tự tính lại** thành tiền, chi phí, thuế theo dữ liệu được chuyển.

## Bản Tài chính tự hạch toán hóa đơn

> Bản Tài chính khi đồng bộ hóa đơn từ **thuế/email**, nếu hóa đơn **đã hợp lệ** thì **tự duyệt và tạo tự động chứng từ**.

Xem chi tiết cơ chế này tại [Hạch toán tự động hóa đơn mua vào](mua-hang-ke-toan.md).

## Báo cáo đối chiếu hai bản

Ba báo cáo **thêm mới** để phát hiện chênh lệch giữa Quản trị và Tài chính:

1. **So sánh bảng cân đối phát sinh tài khoản** — so sánh số dư và phát sinh ở hai bản.
2. **So sánh bảng cân đối phát sinh công nợ** — so sánh số dư và phát sinh công nợ.
3. **So sánh tổng hợp nhập xuất tồn theo kho** — so sánh tồn kho ở hai bản.

<style>
.yes { color: #2e7d32; }
.no { color: #c62828; }
</style>
