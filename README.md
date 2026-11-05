# Sổ từ vựng TOEIC

Trang ôn từ vựng TOEIC cá nhân, chạy trên Cloudflare (Workers static assets).
- Nội dung trang: `public/index.html`
- Cấu hình: `wrangler.jsonc`
Mỗi commit mới lên nhánh `main`, Cloudflare tự triển khai lại trang.

## Bộ học tự tạo
- Trang chủ có thẻ **Tạo bộ học mới** và mục **Bộ học của bạn**.
- Nhập tay hoặc tải file `.docx`, `.xlsx`, `.csv`, `.txt`; trang tự tách từ, loại từ, phiên âm, nghĩa, ví dụ, từ đồng nghĩa và tạo đủ 8 cách ôn.
- Dữ liệu lưu trong trình duyệt (`localStorage`, khóa `toeic-my-sets-v1`); có nút sao lưu/khôi phục file JSON.
- Thư viện đọc file nằm trong `public/lib/` (mammoth 1.8.0 cho Word, SheetJS 0.18.5 cho Excel), chỉ tải khi cần.
- Nút “Tự bổ sung phần còn thiếu” dùng dictionaryapi.dev (phiên âm, loại từ, ví dụ, đồng nghĩa) và MyMemory (dịch nghĩa).
