# BÁO CÁO SỬ DỤNG AI CÓ KIỂM SOÁT (AI USAGE REPORT) - BUỔI 2
## MÔN: PHÁT TRIỂN ỨNG DỤNG WEB / THƯƠNG MẠI ĐIỆN TỬ - UEH
- **Giảng viên hướng dẫn:** TS. Nguyễn Mạnh Tuấn
- **Sinh viên:** Huỳnh Thế An - **MSSV:** 31241021983
- **Dự án:** Showroom & Đặt cọc Ô tô điện VinFast Trực Tuyến

### Nguyên tắc thực hành:
*"Chủ động đặt câu hỏi định hướng, tiếp nhận gợi ý có chọn lọc, đối chiếu thực tế nghiệp vụ TMĐT xe hơi, tự tay kiểm tra và sửa lỗi trên mã nguồn thật."*

### Prompt 1: Rà soát & Phân tích cấu trúc HTML từ Buổi 1
- **Nội dung Prompt:**
  > *"Tôi đang làm bài tập cá nhân môn Phát triển ứng dụng thương mại điện tử (UEH). Trong Buổi 1, tôi đã khảo sát website VinFast và dựng giao diện đặt cọc xe điện. Hãy giúp tôi: 1. Xác định những thành phần HTML đã có; 2. Chỉ ra các thành phần HTML còn thiếu hoặc chưa chuẩn Semantic; 3. Nêu 3 vấn đề về Box Model và bố cục; 4. Đề xuất thứ tự cải tiến từ cấu trúc HTML5 đến Flexbox và CSS Grid. Chưa viết lại toàn bộ mã nguồn."*
- **Kết quả AI phản hồi:** AI nhận diện mã nguồn đã có cấu trúc cơ bản, tuy nhiên thanh điều hướng đang dùng thẻ `<span>` thay vì thẻ `<a>` và danh sách `<ul>/<li>`. Thẻ xe chưa có nút xem chi tiết và các thẻ chưa có trạng thái `:focus-visible`.
- **Phần tự điều chỉnh của sinh viên:** Em lập bảng so sánh 3 vấn đề tồn tại (Cấu trúc Semantic, Box Model cho thẻ xe, Flexbox/Grid bố cục) và xác định rõ phạm vi cải tiến tập trung vào thanh điều hướng Header và lưới 4 dòng xe chiến lược.

### Prompt 2: Hướng dẫn cấu trúc HTML5 Semantic cho thẻ xe và menu
- **Nội dung Prompt:**
  > *"Tôi muốn chuẩn hóa Semantic Web theo yêu cầu của Thầy Tuấn: 1. Chuyển đổi thanh điều hướng menu từ span sang cấu trúc thẻ `<nav>`, `<ul>`, `<li>`, `<a>`; 2. Đặt thuộc tính `alt` chi tiết cho từng dòng xe VF 3, VF 6, VF 7, VF 9; 3. Bổ sung cụm nút hành động gồm nút 'Xem chi tiết' và 'Đặt cọc giữ xe' bằng Flexbox. Hãy đưa ra giải pháp ngắn gọn."*
- **Kết quả AI phản hồi:** AI cung cấp mẫu thẻ `<article class="ev-card">` và danh sách menu `<ul class="nav-list">`.
- **Phần tự điều chỉnh của sinh viên:** Em bổ sung thêm các thuộc tính hỗ trợ tiếp cận (A11y) như `aria-label="Điều hướng chính website"` trên thẻ `<nav>`, `aria-label="Bảng màu ngoại thất"` cho bảng màu xe, và gán `role="button"` cùng `tabindex="0"` cho các chấm chọn màu sơn.


### Prompt 3: Cấu hình Box Model & Giải quyết tỷ lệ ảnh xe không méo
- **Nội dung Prompt:**
  > *"Làm thế nào để kiểm soát Box Model của thẻ xe điện bằng CSS thuần: 1. Sử dụng `box-sizing: border-box`; 2. Điều chỉnh `padding` và `border-radius`; 3. Giữ tỉ lệ hình ảnh xe hơi luôn chuẩn 16:10 và không bị méo góc nhìn khi kích thước màn hình thay đổi?"*
- **Kết quả AI phản hồi:** AI giải thích Box Model và gợi ý dùng thuộc tính `aspect-ratio: 16 / 10; object-fit: cover;`.
- **Phần tự điều chỉnh của sinh viên:** Ban đầu AI để `margin: 15px` cho từng thẻ xe, nhưng em nhận thấy khi dùng CSS Grid thì việc quản lý khoảng cách bằng `gap: 24px;` ở phần tử cha `.ev-grid` là giải pháp chuẩn mực hơn nhiều. Do đó, em đưa `margin` của `.ev-card` về `0` để tránh lỗi cộng dồn khoảng cách.


### Prompt 4: Bố trí lưới xe điện bằng CSS Grid và xử lý lệch đáy nút bấm
- **Nội dung Prompt:**
  > *"Tôi đang dùng CSS Grid cho danh sách 4 xe điện với `grid-template-columns: repeat(4, minmax(0, 1fr))`. Tuy nhiên, khi tên xe có độ dài khác nhau, chiều cao các thẻ bị chênh lệch nhẹ và cụm nút đặt cọc bị so le đáy. Làm thế nào để giải quyết vấn đề này mà không cần code JavaScript?"*
- **Kết quả AI phản hồi:** AI gợi ý giải pháp kết hợp Flexbox trên thẻ cha và đặt `margin-top: auto` cho khối nút con.
- **Phần tự điều chỉnh của sinh viên:** Em trực tiếp áp dụng:
  1. Thêm `display: flex; flex-direction: column; justify-content: space-between;` cho `.ev-card`.
  2. Khống chế tiêu đề xe tối đa 2 dòng bằng `-webkit-line-clamp: 2` và `height: 46px`.
  3. Đặt `margin-top: auto` cho `.card-action`.  
  *Kết quả:* Tất cả các nút bấm trên hàng lưới đều thẳng tắp, đẹp mắt.


### Prompt 5: Tối ưu tương tác bàn phím (:focus-visible) theo chuẩn WCAG
- **Nội dung Prompt:**
  > *"Làm thế nào để bổ sung hiệu ứng hover mượt mà cho thẻ xe và thêm viền focus-visible khi người dùng duyệt web bằng phím Tab mà không gây ảnh hưởng khi bấm chuột?"*
- **Kết quả AI phản hồi:** AI đưa ra cú pháp `:focus-visible { outline: 3px solid #f59e0b; outline-offset: 3px; }`.
- **Phần tự điều chỉnh của sinh viên:** Em đã kiểm tra trực tiếp trên trình duyệt bằng cách không dùng chuột, chỉ dùng phím `Tab` để di chuyển từ Logo -> Menu -> Chấm màu xe -> Nút Chi tiết -> Nút Đặt cọc. Viền màu cam hổ phách hiển thị rất rõ ràng, tương phản hoàn hảo trên nền tối (Dark Theme) của website VinFast.
