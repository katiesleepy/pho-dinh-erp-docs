# Mẫu kết xuất: BKMV & Bảng kê hạch toán

Hai mẫu Excel là **trọng tâm hiện tại của dự án**. Mỗi mẫu có bản **gốc** (hiện có của phần mềm) và bản **chỉnh** (khách hàng yêu cầu).

| Sheet | Mô tả |
|---|---|
| **BKMV (gốc)** | Mẫu xuất hiện tại: **11 cột** — MST đơn vị bán, Tên đơn vị bán, Ký hiệu, Số hóa đơn, Tính chất hóa đơn, Ngày hóa đơn, Tiền chưa thuế, Mã thuế, Tiền thuế, Tổng tiền, Đơn vị |
| **BKMV (chỉnh)** | Giữ cấu trúc theo **TT80/2021** (cột A→M), **sắp xếp theo ngày tăng dần**, thêm **21 cột mới** |
| **HachToan (gốc)** | Mẫu hạch toán hiện tại: **26 cột** theo từng dòng hàng |
| **HachToan (chỉnh)** | Thêm **19 cột mới** |
| **Note1 – Note8** | Dữ liệu mẫu và hình minh họa tham chiếu |

---

## Yêu cầu chung cả 2 bảng

!!! important "Ba quy tắc bắt buộc"
    1. **Số hóa đơn quy về 8 chữ số** — ví dụ số `12` → `00000012`
    2. Thêm cột **tên chi nhánh viết tắt / MST người mua**
    3. Cho phép **chọn nhiều đơn vị (chi nhánh)** khi xuất bảng kê

---

## BKMV (chỉnh) — 21 cột thêm mới

`STT` · `Mẫu số HĐ` · `Tên hàng hóa, dịch vụ` · `Tổng tiền chiết khấu thương mại` · `Tổng tiền phí` · `Nguồn HĐ` · `Họ tên người mua hàng` · `Tên đơn vị mua` · `Trạng thái hóa đơn` · `Nội dung TBSS 04SS` · `Hóa đơn liên quan` · `Địa chỉ đơn vị mua` · `Địa chỉ NCC` · `Ngày ký` · `Ngày cấp mã` · `Ngày tạo` · `Kết quả kiểm tra` · `Link tra cứu` · `Mã tra cứu` · `Căn cước công dân` · `Kết quả kiểm tra hóa đơn`

### Yêu cầu chi tiết theo cột

| Cột | Yêu cầu chỉnh sửa |
|---|---|
| **Số hóa đơn** | Quy về **8 chữ số** (số `12` → `00000012`) |
| **Tên hàng hóa, dịch vụ** | Lấy **dòng nội dung đầu tiên** trên hóa đơn. Phải lấy **theo hóa đơn trên email** vì nhiều hóa đơn trên web thuế không thể hiện tên hàng hóa dịch vụ (sẽ để trống nếu chỉ lấy từ web thuế) |
| **Thuế suất (%)** | Đổi tên cột **"Mã thuế" → "Thuế suất (%)"**. Hóa đơn nhiều thuế suất phải **tách thành nhiều dòng**, mỗi dòng 1 thuế suất; ghi rõ ký hiệu giống web thuế (`0%`, `KKKNT`, `KCT`…) thay vì để `00` |
| **Nguồn HĐ** | Thêm cột thể hiện nguồn lấy hóa đơn (*Tải từ TCT*, *Email*); ưu tiên theo thứ tự **Email → Tải từ TCT** |
| **Trạng thái hóa đơn** | Lấy đúng trạng thái web thuế (*Hóa đơn mới*, *Hóa đơn điều chỉnh*, *Hóa đơn thay thế*…); đổi tên **"Hóa đơn gốc" → "Hóa đơn mới"** |
| **Nội dung TBSS 04SS** | Lấy nội dung Thông báo sai sót 04SS trên web thuế |
| **Hóa đơn liên quan** | Lấy thông tin hóa đơn liên quan trên web thuế (hóa đơn bị thay thế thì hóa đơn nào thay thế); áp dụng khi **cùng MST** |
| **Kết quả kiểm tra** | Đối chiếu với cột **Ghi chú** bên sheet HachToan |

---

## HachToan (chỉnh) — 19 cột thêm mới

`Số hóa đơn gốc` · `Tên sản phẩm_Số HĐ` · `Đơn vị tính quy đổi` · `Số lượng quy đổi` · `NỢ` · `CÓ` · `Trạng thái hóa đơn` · `Họ tên người mua hàng` · `Tên đơn vị mua` · `MST đơn vị mua` · `Nguồn HĐ` · `Nội dung TBSS 04SS` · `Hóa đơn liên quan` · `Căn cước công dân` · `Tổng tiền chiết khấu thương mại` · `Tổng tiền phí` · `Kết quả kiểm tra hóa đơn` · `Link tra cứu` · `Mã tra cứu`

### Yêu cầu chi tiết theo cột

| Cột | Yêu cầu chỉnh sửa |
|---|---|
| **Số hóa đơn** | Quy về 8 chữ số |
| **Trạng thái (Chờ duyệt)** | :material-help: Cần **làm rõ mục đích sử dụng** của cột này |
| **Đơn vị tính quy đổi** | ĐVT **không có trong danh mục quy đổi** thì **giữ nguyên** khi chuyển qua cột này |
| **Số lượng quy đổi** | Tính theo ĐVT quy đổi tương ứng |
| **NỢ** | Xác định theo **danh mục mã hàng** |
| **CÓ** | Xác định theo **danh mục nhà cung cấp** |
| **Thuế suất** | Ghi rõ thuế suất từng mặt hàng: `0%`, `5%`, `8%`, `10%`, `KCT`, `KKKNT`… |
| **Trạng thái hóa đơn** | Đổi "Hóa đơn gốc" → "Hóa đơn mới"; lấy đúng trạng thái web thuế |
| **Ngày tạo** | :material-help: Cần **xác định rõ nguồn lấy dữ liệu** |
| **Nguồn HĐ** | Thể hiện nguồn: *Tải từ TCT*, *Email*, *Upload*; ưu tiên **Email → Upload → Tải từ TCT** |
| **Nội dung TBSS 04SS** | Lấy nội dung TBSS 04SS trên web thuế |
| **Hóa đơn liên quan** | Lấy trên web thuế, áp dụng khi **cùng MST** |

---

## Bảng đối chiếu HachToan (chỉnh): Đã có / Chưa có

### :material-check-circle: 22 cột đã có

MST đơn vị bán · Tên đơn vị bán · Mẫu số HĐ · Ký hiệu · Số hóa đơn · Ngày hóa đơn · Trạng thái *(trạng thái duyệt)* · Tiền chưa thuế · Mã thuế · Tiền thuế · Tổng tiền · Tên sản phẩm · Đơn vị tính · Số lượng · Giá · Tiền trước thuế · Thuế suất · Tiền thuế *(dòng cuối mỗi HĐ)* · Tổng tiền · Ngày ký · Ngày tạo · Ghi chú

### :material-close-circle: 19 cột chưa có

| # | Cột chưa có | Ghi chú |
|:---:|---|---|
| 1 | **Số hóa đơn gốc** | Hiện chỉ có *Số hóa đơn*; cần thêm số HĐ gốc cho HĐ thay thế/điều chỉnh |
| 2 | **Tên sản phẩm_Số HĐ** | Ghép *Tên sản phẩm* + *Số HĐ* |
| 3 | **Đơn vị tính QUY ĐỔI** | Theo danh mục quy đổi; không có thì giữ nguyên |
| 4 | **Số lượng QUY ĐỔI** | Theo ĐVT quy đổi tương ứng |
| 5 | **NỢ** | TK Nợ theo danh mục mã hàng |
| 6 | **CÓ** | TK Có theo danh mục nhà cung cấp |
| 7 | **Trạng thái hóa đơn** | Đổi từ *Tính chất hóa đơn* + lấy trạng thái web thuế |
| 8 | **Họ tên người mua hàng** | |
| 9 | **Tên đơn vị mua** | Hiện chỉ có 1 cột gộp *Tên đơn vị mua/bán* |
| 10 | **MST đơn vị mua** | Hiện chỉ có 1 cột gộp *MST đơn vị mua/bán* |
| 11 | **Nguồn HĐ** | Email / TCT / Upload; ưu tiên **Email → Upload → TCT** |
| 12 | **Nội dung TBSS 04SS** | Lấy trên web thuế |
| 13 | **Hóa đơn liên quan** | HĐ thay thế/điều chỉnh liên quan (cùng MST) |
| 14 | **Căn cước công dân** | |
| 15 | **Tổng tiền chiết khấu thương mại** | Hiện chỉ có *Tiền chiết khấu* ở mức dòng, thiếu tổng ở mức HĐ |
| 16 | **Tổng tiền phí** | |
| 17 | **Kết quả kiểm tra hóa đơn** | Hiện đang gộp trong cột *Ghi chú* |
| 18 | **Link tra cứu** | |
| 19 | **Mã tra cứu** | |

---

## Hai cột Arito xác nhận KHÔNG lấy được

!!! danger "Phản hồi 02/07/2026"
    Cột **Nội dung TBSS 04SS** và cột **Hóa đơn liên quan** — Arito xác nhận **sẽ không lấy được**.

    Hai cột này xuất hiện ở **cả BKMV (chỉnh) và HachToan (chỉnh)**. Cần phương án thay thế hoặc chấp nhận nhập thủ công.
