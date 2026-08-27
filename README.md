# Phổ Đình – ERP Arito · Cơ sở tri thức

Kho tài liệu và kiến thức của dự án triển khai hệ thống **ERP Arito** cho **Công ty TNHH MTV Phổ Đình**.

📖 **Trang web tra cứu:** *(link GitHub Pages sẽ hiện ở đây sau khi bật Pages)*

## Nội dung

| Thư mục | Nội dung |
|---|---|
| `docs/01-tong-quan/` | Về doanh nghiệp, ký hiệu & thuật ngữ |
| `docs/02-danh-muc/` | Tài khoản kế toán, KH/NCC, vật tư, tài sản, template import |
| `docs/03-tckt/` | Chuyển dữ liệu Quản trị↔Tài chính, mua hàng, bán hàng, quỹ, báo cáo |
| `docs/04-mua-hang/` | Quy trình mua hàng, phiếu nhu cầu, đơn đặt hàng, R&D–NXU, báo giá |
| `docs/05-hoa-don-dau-vao/` | Yêu cầu phần mềm hóa đơn điện tử đầu vào, mẫu BKMV & Hạch toán |
| `docs/06-gia-thanh/` | Giá thành xưởng và giá thành chi nhánh |
| `docs/07-bieu-mau-in/` | Mẫu in m61 |
| `docs/08-hop-va-quyet-dinh/` | Meeting recap, dòng thời gian, việc còn tồn |
| `docs/assets/files/` | Toàn bộ file gốc: docx, xlsx, pdf, rdlc |

## Chạy thử trên máy

```bash
pip install mkdocs-material
mkdocs serve
```

Mở http://127.0.0.1:8000

## Cập nhật nội dung

Sửa file `.md` trong `docs/` → commit → push. GitHub Actions tự build và deploy.

Xem hướng dẫn chi tiết tại [docs/cach-cap-nhat.md](docs/cach-cap-nhat.md).

## Bật GitHub Pages (làm 1 lần)

Vào **Settings → Pages → Build and deployment → Source: GitHub Actions**.
