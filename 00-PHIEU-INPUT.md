# 00 — PHIẾU INPUT (điền xong là chạy) — Threads ⇄ Lark

> **Ô I của ITTO**: chuẩn bị TRƯỚC khi bấm chạy. Chi tiết: `README.md`, `TRIEN-KHAI.md`.
> Soát hợp đồng: `node check-itto.mjs`. **Lưu ý:** repo là FORK từ hangchinaaibusiness.

| # | Việc | Điền / xác nhận | Xong? |
|---|---|---|---|
| 1 | **App Lark** + quyền `bitable:app` + thêm app vào Base | LARK_APP_ID `cli_…`, LARK_BASE_ID `…` | ☐ |
| 2 | **Bảng Threads**: `src/init-tables.js` (event `init-tables`) | THREADS_TABLE_ID `tbl…`, THREADS_TABLE_NAME | ☐ |
| 3 | **Threads token**: `src/get-token.js` → THREADS_ACCESS_TOKEN + THREADS_USER_ID | ✅ / ❌ | ☐ |
| 4 | **FTP host media** (để Threads tải ảnh/video công khai) | HANGCHINA_FTP_HOST/​USER/​PASS, THREADS_MEDIA_BASE_URL | ☐ |
| 5 | **Nạp GitHub** — Secret + Variable | ✅ / ❌ | ☐ |
| 6 | **Preflight**: `node check-itto.mjs` → XANH | ✅ / ❌ | ☐ |
| 7 | **Nối nút/lịch** Lark (đăng / kéo số liệu) | ✅ / ❌ | ☐ |

**Secrets:** `LARK_APP_SECRET` · `THREADS_ACCESS_TOKEN` · `HANGCHINA_FTP_HOST` · `HANGCHINA_FTP_USER` · `HANGCHINA_FTP_PASS`
**Variables:** `LARK_APP_ID` · `LARK_DOMAIN` · `LARK_BASE_ID` · `THREADS_USER_ID` · `THREADS_TABLE_ID` · `THREADS_TABLE_NAME` · `THREADS_MEDIA_BASE_URL`

**event_type (3):** `init-tables` · `dang-threads` · `so-lieu-threads`.

> Threads yêu cầu URL media công khai (ảnh/video) → bộ này host qua FTP (`HANGCHINA_*`) rồi
> truyền link vào API. Vì là fork, kiểm tra tab **Actions** đã bật workflow chưa (fork mặc định tắt).
