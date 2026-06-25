# Hướng dẫn xử lý khi không xem được video trên Mapstudy

Trang web tĩnh (1 file `index.html`) chuyển từ file PDF hướng dẫn, để học sinh đọc dễ hiểu hơn.

## Cấu trúc

```
site/
├── index.html       # Toàn bộ nội dung + giao diện
├── images/          # Ảnh chụp màn hình trích từ PDF
├── vercel.json      # Cấu hình cache cho Vercel
└── README.md
```

## Xem thử trên máy

Mở trực tiếp `index.html` bằng trình duyệt, hoặc chạy:

```bash
cd site
python3 -m http.server 8080
# Mở http://localhost:8080
```

## Đưa lên Vercel

**Cách 1 — Kéo thả (nhanh nhất, không cần lệnh):**
1. Vào https://vercel.com → đăng nhập.
2. Nén thư mục `site` hoặc kéo thẳng thư mục vào ô **Deploy**.
3. Xong — Vercel cấp link `https://...vercel.app`.

**Cách 2 — Dùng Vercel CLI:**
```bash
npm i -g vercel
cd site
vercel          # làm theo hướng dẫn, chọn thư mục hiện tại
vercel --prod   # đưa lên bản chính thức
```

**Cách 3 — Qua Git (GitHub/GitLab):**
1. Đẩy thư mục `site` lên một repo.
2. Trên Vercel: **Add New → Project → Import** repo đó.
3. Mục **Root Directory** chọn `site` (nếu repo có thêm thư mục khác), **Framework Preset** để **Other**, rồi **Deploy**.
