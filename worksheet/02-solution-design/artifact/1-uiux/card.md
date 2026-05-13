# Card: Giao diện cảnh báo rủi ro dữ liệu (UI/UX)

## 1. Thông tin chung
- **Lớp giải pháp**: Giao diện (UI/UX)
- **Rủi ro giải quyết**: T-02 — OCR đọc sai số liệu do ảnh mờ/nhiễu.
- **Hành động phòng vệ**: Thông báo + Phát hiện.

---

## 2. Thiết kế giải pháp
### Cách vận hành
Khi AI trích xuất dữ liệu từ chứng từ, các ô có độ tự tin (confidence score) thấp dưới 85% sẽ được bôi đỏ hoặc vàng. Một tooltip sẽ hiện ra yêu cầu người dùng đối chiếu lại với bản gốc. Nút "Tiếp tục" sẽ bị vô hiệu hóa cho đến khi người dùng xác nhận hoặc sửa lại các ô này.

### Tại sao giải pháp này hiệu quả?
Giải pháp này buộc người dùng phải "Human-in-the-loop", không cho phép họ tin tưởng mù quáng vào AI. Nó chuyển trách nhiệm xác thực sang người dùng một cách minh bạch.

---

## 3. Demo
- **Định dạng**: ASCII UI Sketch
- **Mô tả**: Bản phác thảo màn hình trích xuất dữ liệu với các cảnh báo lỗi.
- **Link**: [demo.md](./demo.md)
