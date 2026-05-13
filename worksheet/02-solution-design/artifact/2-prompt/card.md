# Card: Chỉ dẫn hệ thống kiểm soát logic (Prompt Engineering)

## 1. Thông tin chung
- **Lớp giải pháp**: Chỉ dẫn AI (Prompt)
- **Rủi ro giải quyết**: T-02 — OCR đọc sai số liệu.
- **Hành động phòng vệ**: Ngăn + Hỏi lại.

---

## 2. Thiết kế giải pháp
### Cách vận hành
Thiết lập System Prompt yêu cầu AI thực hiện "Self-Correction" và "Logic Check". Trước khi trả về kết quả JSON, AI phải tự kiểm tra xem các con số trích xuất có khớp với nhau không (Ví dụ: Số thuế khấu trừ phải bằng khoảng 10% thu nhập chịu thuế). Nếu thấy bất hợp lý, AI phải trả về cờ cảnh báo `warning: logic_mismatch`.

### Tại sao giải pháp này hiệu quả?
Tận dụng khả năng suy luận (reasoning) của LLM để phát hiện các lỗi của Vision/OCR. AI không chỉ "nhìn" mà còn "hiểu" mối quan hệ giữa các con số.

---

## 3. Demo
- **Định dạng**: Markdown (Prompt Structure)
- **Mô tả**: Cấu trúc System Instruction cho Gemini.
- **Link**: [demo.md](./demo.md)
