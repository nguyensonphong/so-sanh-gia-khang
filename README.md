# Hệ Thống So Sánh Giá Thị Trường - Điện Máy Gia Khang

Hệ thống dashboard giám sát, đối chiếu giá thị trường tự động giữa **Điện Máy Gia Khang** và các chuỗi bán lẻ điện máy hàng đầu Việt Nam: **Điện Máy Xanh**, **Điện Máy Chợ Lớn**, và **Meta.vn**.

🔗 **Website Live Dashboard:** [https://nguyensonphong.github.io/so-sanh-gia-khang/](https://nguyensonphong.github.io/so-sanh-gia-khang/)  
🔒 **Mật khẩu truy cập nội bộ:** `GK-1234`

---

## 🎯 Tính Năng Nổi Bật

1. **Bảo Mật Đầu Cuối (Client-side AES-256-GCM):**
   - Toàn bộ cơ sở dữ liệu đối thủ được mã hóa bằng chuẩn quân đội AES-256-GCM và hàm dẫn xuất khóa PBKDF2 (250,000 vòng lặp).
   - Dữ liệu hoàn toàn an toàn ngay cả khi repo được lưu trữ công khai trên GitHub.

2. **Dữ Liệu Toàn Diện (4 Sàn · 5 Ngành Hàng):**
   - **Tivi, Máy Lạnh, Máy Giặt, Tủ Lạnh, Máy Sấy Quần Áo**.
   - Hơn **5,380+ sản phẩm** thu thập thực tế từ 4 sàn.
   - **1,683 model** được chuẩn hóa khớp chính xác giữa Điện Máy Gia Khang và đối thủ.

3. **Chỉ Số KPI & Trực Quan Hóa (Chart.js):**
   - 🔴 **Cần hạ giá:** Model mà Điện Máy Gia Khang đang cao hơn giá thấp nhất thị trường.
   - 🟡 **Lợi thế giá rẻ (≥5%):** Model Gia Khang rẻ hơn đối thủ từ 5% trở lên.
   - 🟢 **Cạnh tranh (±5%):** Mức giá bám sát thị trường.
   - Biểu đồ phân bổ tỷ trọng cảnh báo theo từng ngành hàng & đối thủ bán rẻ nhất.

4. **Công Cụ Lọc & Phân Tích Chuyên Sâu:**
   - Tìm kiếm tức thì theo Model, Tên sản phẩm, Thương hiệu (Samsung, LG, Daikin, Panasonic, Casper, Aqua, Sharp...).
   - Sắp xếp theo % chênh lệch, giá chênh lệch VNĐ, giá Gia Khang.
   - Xem chi tiết giá và link trực tiếp sang từng website đối thủ để kiểm tra thực tế.
   - Xuất dữ liệu ra file Excel (CSV chuẩn UTF-8).

5. **Theo Dõi Biến Động Giá & Sản Phẩm Mới:**
   - Tab biến động ghi nhận lịch sử tăng giá, giảm giá, sản phẩm mới mở bán hoặc tạm hết hàng giữa các chu kỳ quét.

6. **Tự Động Hóa 09:00 AM Hàng Ngày:**
   - Script Sidecar tự động thu thập lúc 09:00 AM mỗi ngày, nạp Supabase, đồng bộ Lark Base và tự động cập nhật GitHub Pages.

---

## 🛠️ Công Nghệ Sử Dụng

- **Thu thập dữ liệu:** Firecrawl API, Node.js + Chrome CDP (vượt Cloudflare), Python BeautifulSoup.
- **Lưu trữ & Chuẩn hóa:** PostgreSQL 17 (Supabase), View chuẩn hóa model key.
- **Frontend Dashboard:** Single Page Application (HTML5, Tailwind CSS, Chart.js, Lucide Icons).
- **Mã hóa:** Web Crypto API (SubtleCrypto) + Node.js Crypto PBKDF2 / AES-256-GCM.
- **Triển khai:** GitHub Pages & GitHub Actions/Sidecars.
