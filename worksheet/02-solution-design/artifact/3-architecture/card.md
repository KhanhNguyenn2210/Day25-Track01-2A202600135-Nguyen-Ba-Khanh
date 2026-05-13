# Card: Kiến trúc kiểm tra chéo đa tầng (Architecture)

## 1. Thông tin chung
- **Lớp giải pháp**: Kiến trúc dữ liệu (Architecture)
- **Rủi ro giải quyết**: T-02 — OCR đọc sai số liệu.
- **Hành động phòng vệ**: Ngăn + Khắc phục.

---

## 2. Thiết kế giải pháp
### Cách vận hành
Sử dụng kiến trúc "Double OCR Pipeline":
1. **Pipeline A**: Sử dụng Gemini 1.5 Pro (Multimodal) để trích xuất ngữ cảnh và con số.
2. **Pipeline B**: Sử dụng một engine OCR chuyên biệt cho con số (như AWS Textract hoặc Google Document AI).
3. **Mô-đun đối chiếu (Consensus Module)**: Một service nhỏ so sánh kết quả từ 2 Pipeline. Nếu kết quả lệch nhau vượt quá ngưỡng cho phép, hệ thống sẽ trigger trạng thái "Cần kiểm tra lại" và gửi thông báo cho người dùng hoặc admin.

### Tại sao giải pháp này hiệu quả?
Giảm thiểu "Single point of failure". Việc hai mô hình khác kiến trúc cùng sai ở một vị trí là rất thấp.

---

## 3. Demo
- **Định dạng**: Mermaid Diagram
- **Mô tả**: Sơ đồ luồng dữ liệu kiểm tra chéo.
- **Link**: [demo.md](./demo.md)
