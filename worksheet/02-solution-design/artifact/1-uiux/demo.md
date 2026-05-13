# Demo: Giao diện cảnh báo OCR (ASCII Sketch)

```text
+-------------------------------------------------------------+
|  [X] QUYẾT TOÁN THUẾ TNCN - KIỂM TRA DỮ LIỆU                |
+-------------------------------------------------------------+
|                                                             |
|  [!] Cảnh báo: AI nhận diện một số trường không rõ nét.     |
|      Vui lòng kiểm tra lại với chứng từ gốc.                |
|                                                             |
|  +---------------------------+   +-----------------------+  |
|  | Chứng từ gốc (Ảnh)        |   | Kết quả trích xuất    |  |
|  |                           |   |                       |  |
|  | [ Ảnh chụp chứng từ ]     |   | 1. Mã số thuế:        |  |
|  | [ Vùng thu nhập:      ]   |   | [ 8034567890       ]  |  |
|  | [ 88.000.000 VNĐ      ]   |   |                       |  |
|  |                           |   | 2. Thu nhập chịu thuế:|  |
|  |                           |   | [ 00.000.000       ] <--- [!] SAI (Bôi đỏ)
|  |                           |   |   (Độ tự tin: 62%)    |  |
|  |                           |   |                       |  |
|  |                           |   | 3. Số thuế đã khấu trừ|  |
|  |                           |   | [ 8.800.000        ]  |  |
|  +---------------------------+   +-----------------------+  |
|                                                             |
|  [ Sửa lại dữ liệu ]   [ Tôi xác nhận dữ liệu đã đúng ]     |
|                                                             |
+-------------------------------------------------------------+
| [ ] Đồng ý với điều khoản bảo mật dữ liệu                   |
|                                                             |
|                   [ TIẾP TỤC (Vô hiệu hóa) ]                |
+-------------------------------------------------------------+
```

### Giải thích Demo:
- **Ô số 2**: AI đọc nhầm "88" thành "00". Hệ thống bôi đỏ và hiển thị độ tự tin thấp.
- **Nút Tiếp tục**: Bị xám (disabled) cho đến khi người dùng tương tác với ô lỗi.
