

## Phần 1. Phân tích bài toán

AI không đọc văn bản theo từng từ nguyên vẹn như con người mà chia nhỏ văn bản thành các đoạn ký tự gọi là **Token**. Khi truyền dữ liệu vào hoặc ra từ mô hình AI, số lượng Token càng lớn thì chi phí xử lý (tiền gọi API) càng cao và thời gian hệ thống phản hồi càng lâu.

Markdown giúp AI xử lý nhanh hơn HTML vì các lý do sau:

* **Tối giản ký tự:** Để định dạng văn bản, Markdown sử dụng các ký tự đơn giản. Ví dụ: in đậm chữ "Nông nghiệp" trong Markdown chỉ cần `**Nông nghiệp**` (khoảng 15 ký tự).
* **HTML có nhiều thẻ thừa:** Trong HTML, việc in đậm tương tự phải viết là `<strong>Nông nghiệp</strong>` (khoảng 28 ký tự).
* **Tác động tới Token:** Việc dùng HTML làm tăng đáng kể số lượng Token không cần thiết chỉ để chứa các thẻ đóng/mở (`<p>`, `<div>`, `<ul>`, `<li>`). Markdown loại bỏ các thẻ rườm rà này, giúp giảm số lượng Token, từ đó giúp AI sinh dữ liệu nhanh hơn và tiết kiệm chi phí hệ thống.

---

## Phần 2. So sánh & Đánh giá

### 1. Bảng so sánh Markdown và HTML

| Tiêu chí | Markdown | HTML |
| :--- | :--- | :--- |
| **Số lượng ký tự & Token** | Tốn ít Token (chỉ dùng các ký tự ngắn như `*`, `#`) | Tốn nhiều Token do phải kèm các thẻ lệnh đóng/mở |
| **Độ dễ đọc (Human-readable)** | Dễ đọc, gần gũi với văn bản thuần | Khó đọc hơn vì bị lẫn các thẻ lệnh lập trình |
| **Tốc độ AI xử lý** | Nhanh hơn | Chậm hơn |
| **Khả năng hiển thị** | Trình bày dạng cơ bản (danh sách, in đậm, tiêu đề) | Tùy chỉnh giao diện phức tạp, màu sắc, bố cục linh hoạt |

---

### 2. Giải pháp cho hệ thống "GreenTech"

* **Đề xuất giải pháp:** Sử dụng định dạng **Markdown** để trả về dữ liệu cho hệ thống "GreenTech".
* **Lý do lựa chọn:**
  1. **Tối ưu chi phí & Tốc độ:** Giảm lượng Token thừa giúp GreenTech tiết kiệm chi phí vận hành API. Đồng thời, phản hồi được trả về nhanh chóng, giúp người nông dân nhận câu trả lời ngay lập tức.
  2. **Trải nghiệm người dùng tốt:** Người nông dân cần thông tin dễ hiểu, trực quan. Văn bản Markdown sạch sẽ, không bị rối mắt bởi mã code, hiển thị rõ ràng các danh sách hướng dẫn từng bước.
  3. **Đủ đáp ứng nhu cầu:** Các câu hỏi về tư vấn nông nghiệp chỉ cần các định dạng cơ bản như gạch đầu dòng, bảng ngắn hoặc in đậm các lưu ý quan trọng — đây là những tính năng Markdown xử lý rất tốt.