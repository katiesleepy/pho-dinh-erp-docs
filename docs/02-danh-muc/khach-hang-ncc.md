# Danh mục Khách hàng / Nhà cung cấp

## Nguyên tắc thiết lập

- Dùng để quản lý thông tin đối tượng giao dịch phục vụ **mua hàng, bán hàng, quản lý công nợ**.
- Mỗi đối tượng có **một mã định danh duy nhất**, dùng thống nhất trong toàn hệ thống.
- Một đối tượng có thể **vừa là khách hàng vừa là nhà cung cấp** (danh mục dùng chung một cấu trúc, phân biệt bằng cột `Khách hàng` / `Nhà cung cấp`).

## Thông tin quản lý

Mã đối tượng, tên đối tượng, mã số thuế, địa chỉ, thông tin liên hệ, tài khoản ngân hàng và các thông tin phục vụ quản lý công nợ.

!!! tip "Tra cứu nhanh theo MST"
    Tại màn hình danh mục, nhập **mã số thuế** rồi nhấn biểu tượng tra cứu — hệ thống tự lấy nhanh thông tin doanh nghiệp về.

## Yêu cầu chung — quy tắc mã

> Sử dụng chung **1 bộ mã**, đồng bộ từ bản Quản trị sang bản Tài chính, **10 ký tự**.

- Nếu mã Quản trị và Tài chính **không khớp**, phải chạy chuyển mã từ Quản trị để đồng bộ lại qua Tài chính.
- Trước khi chuyển dữ liệu, Phổ Đình cần đồng nhất bộ mã giữa hai bản; nếu khác biệt thì **gộp mã hoặc đổi mã**.

## Việc còn tồn: chuẩn hóa format mã

Trong buổi họp 02/07/2026, hai bên ghi nhận:

> **Mã Nhà cung cấp và Mã sản phẩm cần được tạo theo 1 định dạng (format) thống nhất.**

Trách nhiệm: **Phổ Đình & Arito** cùng thống nhất quy tắc. Chưa xác định deadline. Xem [Việc còn tồn](../08-hop-va-quyet-dinh/viec-con-ton.md).

## Danh mục vật tư mapping HĐĐV

Vì mỗi nhà cung cấp đặt **một tên khác nhau** cho cùng một mặt hàng, hệ thống bổ sung danh mục mapping riêng. Xem chi tiết tại [Hạch toán tự động hóa đơn mua vào](../03-tckt/mua-hang-ke-toan.md#danh-muc-vat-tu-mapping-hv).
