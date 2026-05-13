---
title: 00 — Bối cảnh sản phẩm cá nhân
section: Day 25 — dùng lại cho mọi cuộc trò chuyện với AI
format: Cá nhân
time: Điền 5 phút đầu buổi
---

# 00-context.md — Bối cảnh sản phẩm cá nhân

## 1. Sản phẩm

- **Tên sản phẩm / bot**: Trợ lý AI Quyết toán thuế TNCN
- **Sản phẩm giúp ai làm gì**: Giúp người làm công ăn lương và freelancer tự quyết toán thuế TNCN bằng cách trích xuất dữ liệu từ chứng từ (OCR), giải thích luật thuế và tối ưu số thuế phải nộp/hoàn.
- **Người dùng gặp sản phẩm ở đâu**: Ứng dụng web/mobile.
- **Giai đoạn hiện tại**: Đang thử nghiệm (MVP).

---

## 2. Phạm vi

**AI được làm gì**

- Trích xuất thông tin từ ảnh chụp chứng từ thuế, CCCD.
- Tóm tắt và giải thích các điều khoản luật thuế dựa trên nguồn dữ liệu đã kiểm duyệt (RAG).
- Gợi ý cách phân bổ người phụ thuộc để tối ưu số thuế.

**AI không được làm gì**

- Không tự động nộp tờ khai lên hệ thống Tổng cục Thuế.
- Không đưa ra lời khuyên pháp lý (legal advice) mang tính cam kết.
- Không truy cập trực tiếp vào tài khoản ngân hàng của người dùng.

**Vì sao có giới hạn này**

- Rủi ro pháp lý cao nếu AI tư vấn sai hoặc thao tác sai trên hệ thống thuế quốc gia. Bảo mật dữ liệu tài chính là ưu tiên hàng đầu.

---

## 3. Người dùng

- **Là ai**: Người đi làm (25-40 tuổi), freelancer, có nhiều nguồn thu nhập, rành công nghệ nhưng không chuyên về kế toán/thuế.
- **Họ hỏi AI khi nào**: Khi bắt đầu mùa quyết toán thuế (tháng 3-4), khi nhận được chứng từ khấu trừ thuế mà không biết điền vào đâu.
- **Họ cần quyết định gì sau khi hỏi AI**: Có tin vào con số AI tính toán để xuất file XML nộp thuế hay không.
- **Khi nào họ dễ bị tổn thương / dễ hiểu sai**: Khi AI dùng thuật ngữ chuyên môn quá phức tạp hoặc khi AI khẳng định chắc chắn một con số mà không có căn cứ rõ ràng.
- **Họ thường tin AI đến mức nào**: Cần người thật hoặc hệ thống kiểm chứng lại vì liên quan đến tiền bạc và pháp lý.

---

## 4. Bối cảnh ngành

- **Sự cố tương tự đã từng xảy ra**: Chatbot tư vấn luật đưa ra thông tin cũ hoặc bịa đặt (hallucination) dẫn đến người dùng bị phạt chậm nộp.
- **Quy định hoặc ràng buộc liên quan**: Luật quản lý Thuế, các nghị định về thuế TNCN, quy định về bảo vệ dữ liệu cá nhân (ND71).
- **Nguồn chính thức nên ưu tiên**: Thư viện pháp luật, Cổng thông tin Tổng cục Thuế.

---

## 5. Ghi chú thêm

- Hệ thống sử dụng Gemini 1.5 Pro cho khả năng OCR và suy luận luật. Cần tập trung vào việc minh bạch nguồn gốc dữ liệu (Citing sources).
