# Quỹ – Ngân hàng

Ngân hàng đang sử dụng: **VietinBank** và **Techcombank**.

## Cập nhật đề nghị chi

### Yêu cầu
- Thêm tính năng **chọn hóa đơn đầu vào** khi thanh toán.
- Thêm trường **đã cọc** → tiền thanh toán tự trừ ra tiền cọc.

### Giải pháp — tab Chi tiết thêm 4 trường

| Trường | Quy tắc |
|---|---|
| **Số hóa đơn** | Chọn từ màn hình **Hóa đơn đầu vào** — mục đích lưu vết thanh toán cho hóa đơn nào |
| **Tiền hóa đơn** | Tự gán theo **tổng tiền hóa đơn** |
| **Tiền cọc** | Người dùng tự nhập số tiền đã cọc trước đó |
| **Tiền thanh toán** | Tự tính: `Tiền hóa đơn − Tiền cọc` |

---

## Giấy báo nợ (tiền ra)

### Yêu cầu
- Khi **chi công nợ**, Phổ Đình lập giấy báo nợ trên phần mềm, sau đó làm báo cáo để đẩy **template lên ngân hàng**.
- **Chi phí ngân hàng, xăng dầu**: tải từ sổ phụ rồi điền template đẩy lên phần mềm.

### Giải pháp

**Báo cáo chuyển khoản ngân hàng (thêm mới):** lấy dữ liệu từ giấy báo nợ, tổng hợp các giấy báo nợ để xuất theo **form mẫu ngân hàng**.

**Import hàng loạt giao dịch xăng dầu — 3 bước:**

1. Tải file import tại màn hình **Giấy báo nợ**.
2. Điền dữ liệu cần đẩy lên hệ thống.
3. Nhấn nút **Lấy dữ liệu từ Excel**, chọn lại file vừa điền để import.

---

## Giấy báo có (tiền vào)

### Yêu cầu
- Tiền vào lấy theo **giao dịch sổ phụ** (chưa chốt được map với giao dịch POS).
- Khi kéo từ POS sẽ kéo thêm cột **mã tham chiếu** để đối chiếu với sổ phụ ngân hàng.
- Bill có tiền về **ngày hôm sau**: điều chỉnh tài khoản, treo vào **131**, sau đó tạo phiếu thu tự động lại để treo tiền cho khớp sổ phụ.

### Giải pháp — luồng xử lý lệch ngày

1. Bill đồng bộ trong ngày, giao dịch ngân hàng ghi nhận ngày hôm sau → người dùng vào bill **điều chỉnh tài khoản Nợ từ 111 → 131**.
2. Các chứng từ thu tiền qua ngân hàng: điều chỉnh **giảm tiền** tương ứng với các hóa đơn được điều chỉnh giảm.
3. Đến khi **tiền về tài khoản**: lập một **Giấy báo nợ** tương ứng để ghi nhận **tăng tiền ngân hàng**.

!!! question "Còn treo"
    Việc **map giao dịch sổ phụ với giao dịch POS** chưa chốt được phương án. Cột **mã tham chiếu** kéo từ POS là cơ sở để đối chiếu.

---

## Phiếu thu/chi không chuyển

Ghi nhận trong họp 15/07/2026 (phân hệ Tổng hợp):

> Tạo **2 quyển** cho các phiếu thu/chi **không chuyển** (từ Quản trị sang Tài chính).
