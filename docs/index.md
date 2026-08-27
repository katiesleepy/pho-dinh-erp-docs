# Cơ sở tri thức dự án Phổ Đình – ERP Arito

Đây là nơi lưu trữ, tra cứu toàn bộ tài liệu và kiến thức của dự án triển khai hệ thống **ERP Arito** cho **Công ty TNHH MTV Phổ Đình**.

!!! tip "Cách dùng trang này"
    Dùng ô **tìm kiếm** ở đầu trang để tra nhanh theo từ khóa tiếng Việt (ví dụ: `04SS`, `giá thành`, `phiếu nhu cầu`, `BKMV`, `m61`, `quy đổi đơn vị tính`). Menu bên trái phân theo phân hệ nghiệp vụ.

## Dự án một phút

| Hạng mục | Thông tin |
|---|---|
| Khách hàng | Công ty TNHH MTV Phổ Đình (thuộc URAETEI GROUP) |
| Ngành nghề | Chuỗi nhà hàng ẩm thực Nhật Bản, thành lập 2009 |
| Nhà cung cấp giải pháp | Arito Solutions |
| Hệ thống | Arito ERP – 01 bản cài đặt, 30 user đăng nhập đồng thời |
| Đơn vị cơ sở | Văn phòng HCM + Xưởng sản xuất KCN Hiệp Phước + 10 chi nhánh nhà hàng |
| MST mẹ | 0308455031 (các MST con: -003, -005, -006, -007, -012, -013, -014, -016, -018) |
| Mã tài liệu BRD | 260727-TLKS/PHODINH-TCKT (lập 27/07/2026) |
| Người lập BRD | Nguyễn Văn Khánh · Người duyệt: Nguyễn Thị Duyên |

## Hai luồng công việc chính

Dự án gồm **hai mảng tách biệt** nhưng liên quan nhau:

<div class="grid cards" markdown>

-   :material-database-sync: **Nâng cấp ERP Arito**

    ---

    Khảo sát và cấu hình lại các phân hệ TCKT, Mua hàng, Bán hàng, Kho, Giá thành, Tài sản/Công cụ. Đặc thù lớn nhất: song song **bản Quản trị** và **bản Tài chính**, có cơ chế chuyển dữ liệu giữa hai bản.

    [:octicons-arrow-right-24: Xem phân hệ TCKT](03-tckt/chuyen-du-lieu.md)

-   :material-receipt-text: **Phần mềm hóa đơn điện tử đầu vào**

    ---

    Tự động thu thập – kiểm tra – cảnh báo lỗi – lưu trữ – hạch toán hóa đơn mua vào đa chi nhánh, để kê khai thuế chính xác và kịp thời.

    [:octicons-arrow-right-24: Xem yêu cầu hóa đơn](05-hoa-don-dau-vao/tong-quan.md)

</div>

## Điều hướng nhanh

| Bạn cần tìm | Vào đây |
|---|---|
| Quy trình mua hàng từ A→Z, các cấp duyệt | [Quy trình mua hàng](04-mua-hang/quy-trinh.md) |
| Nguyên tắc đặt mã KH/NCC/vật tư, template import | [Danh mục](02-danh-muc/khach-hang-ncc.md) · [Template import](02-danh-muc/template-import.md) |
| Chứng từ nào chuyển từ Quản trị sang Tài chính | [Chuyển dữ liệu](03-tckt/chuyen-du-lieu.md) |
| Cách tính giá thành xưởng / chi nhánh | [Giá thành](06-gia-thanh/gia-thanh-xuong.md) |
| Danh sách 26 yêu cầu gốc + phản hồi Arito | [Yêu cầu gốc](05-hoa-don-dau-vao/yeu-cau-goc.md) |
| Chi tiết từng cột BKMV / Hạch toán | [Mẫu kết xuất](05-hoa-don-dau-vao/bkmv-hach-toan.md) |
| Việc còn tồn, ai chịu trách nhiệm | [Việc còn tồn](08-hop-va-quyet-dinh/viec-con-ton.md) |
| Mẫu in đề xuất mua hàng m61 | [Mẫu in m61](07-bieu-mau-in/m61.md) |
| Tải file gốc (docx/xlsx/pdf) | [Tài liệu gốc](tai-lieu-goc.md) |

## Trạng thái tài liệu

Nội dung wiki này được tổng hợp từ các tài liệu khảo sát, meeting recap và bảng yêu cầu tính đến **27/08/2026**. Khi có tài liệu mới, xem [Cách cập nhật](cach-cap-nhat.md).
