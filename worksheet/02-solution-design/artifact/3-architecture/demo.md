# Demo: Sơ đồ kiến trúc Double OCR Pipeline

```mermaid
graph TD
    User((Người dùng)) -->|Upload ảnh chứng từ| App[Giao diện Ứng dụng]
    App -->|Gửi ảnh| Storage[(Bộ nhớ tạm)]
    
    Storage --> P1[Pipeline A: Gemini 1.5 Pro]
    Storage --> P2[Pipeline B: Document AI / OCR Engine]
    
    P1 -->|JSON kết quả A| CM{Consensus Module}
    P2 -->|JSON kết quả B| CM
    
    CM -->|Kết quả khớp| Success[Xuất dữ liệu sang Tờ khai]
    CM -->|Kết quả lệch / Độ tin cậy thấp| Fail[Cảnh báo UI/UX & Highlight ô lỗi]
    
    Fail -->|Người dùng sửa tay| Success
```

### Giải thích:
- **Consensus Module**: Là bộ não của kiến trúc, thực hiện so sánh từng trường dữ liệu.
- **Dữ liệu an toàn**: Chỉ khi cả 2 nguồn cùng đồng thuận thì dữ liệu mới được coi là "sạch" để đi tiếp.
