# Danh mục tài khoản kế toán

## Nguyên tắc thiết lập

- Thiết lập theo hệ thống tài khoản kế toán hiện hành, chuẩn **Thông tư 99**.
- Dùng **thống nhất** trong tất cả phân hệ: tổng hợp, mua hàng, bán hàng, kho.
- Danh mục tài khoản của **bản Quản trị và bản Tài chính phải đồng nhất**, được chuyển sang qua cơ chế chuyển dữ liệu.

## Quy tắc tách chi tiết từng tài khoản

Đây là bảng tra cứu quan trọng nhất khi khai báo hoặc kiểm tra tài khoản:

| Tài khoản | Nội dung | Quy tắc tách chi tiết |
|---|---|---|
| **111** | Tiền mặt | Tách theo **từng chi nhánh** |
| **112** | Tiền gửi ngân hàng | 5–6 tài khoản |
| **128** | Đầu tư nắm giữ đến ngày đáo hạn | Tách theo **thời gian gửi**: ≤ 1 tháng là tương đương tiền; > 1 tháng là khoản đầu tư |
| **131** | Phải thu khách hàng | **Không** tách nhỏ chi tiết — theo dõi công nợ theo đối tượng khách hàng |
| **133** | Thuế GTGT được khấu trừ | Đi theo **cơ quan quản lý thuế** của các chi nhánh |
| **141** | Tạm ứng | **Không** tách nhỏ — theo dõi công nợ nhân viên |
| **211** | Tài sản cố định | **Không** tách chi tiết |
| **242** | Chi phí trả trước | **Không** tách chi tiết |
| **243** | Tài sản thuế thu nhập hoãn lại | **Không** tách chi tiết |
| **331** | Phải trả người bán | Đang tách chi tiết theo NCC → **điều chỉnh gộp chung về tài khoản chung**. Phát sinh ngoại tệ: **VND, USD, JPY** |
| **333** | Thuế và các khoản phải nộp | Tách theo **3 tỉnh**, sau đó theo dõi theo chi nhánh |
| **335** | Chi phí phải trả | Tách theo **chi nhánh** |
| **344** | Nhận ký quỹ, ký cược | **Không** tách chi tiết |
| **511** | Doanh thu bán hàng | Tách theo **3 tỉnh**, sau đó theo dõi theo chi nhánh |
| **521** | Các khoản giảm trừ doanh thu | Tách theo **3 tỉnh**, sau đó theo dõi theo chi nhánh |

!!! warning "Lưu ý về 331"
    Yêu cầu là **gộp** 331 về tài khoản chung thay vì tách chi tiết theo từng NCC như hiện tại. Việc theo dõi công nợ theo NCC vẫn thực hiện được qua mã đối tượng, không cần tách tài khoản.

## Giải pháp thực hiện

- Sử dụng chuẩn Arito — Arito thiết lập danh mục tài khoản theo cấu trúc Thông tư 99.
- Khi phát sinh **chi nhánh mới**, người dùng bấm **Thêm** để tạo thêm tài khoản cho nhánh đó.

## Tài khoản đặc thù cần chú ý

| Tài khoản | Bối cảnh sử dụng trong dự án |
|---|---|
| **136 / 336** | Hạch toán bán hàng nội bộ giữa các chi nhánh (đi tỉnh). Phổ Đình cần rà soát lại luồng hạch toán này — xem [Recap 15/07/2026](../08-hop-va-quyet-dinh/recap-15-07-2026.md) |
| **138** | Ghi nhận nguyên liệu xuất kho **vượt mức hao hụt** cho phép, chờ xử lý — đồng thời giảm chi phí NVL của giá thành |
| **154 / đầu 6** | Kết chuyển chi phí sản xuất trong kỳ — cần khai báo trường **Tài khoản dở dang** ở danh mục vật tư |
| **214 / 811 / 711** | Bút toán thanh lý tài sản — xem [Tài sản & Công cụ](tai-san-cong-cu.md) |
