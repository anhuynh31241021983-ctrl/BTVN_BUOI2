# BÀI TẬP CÁ NHÂN - BUỔI 2: HTML5 & CSS3
## MÔN HỌC: PHÁT TRIỂN ỨNG DỤNG WEB / THƯƠNG MẠI ĐIỆN TỬ (UEH)
- **Giảng viên hướng dẫn:** TS. Nguyễn Mạnh Tuấn (`tuannm@ueh.edu.vn`)
- **Sinh viên thực hiện:** Huỳnh Thế An
- **Mã số sinh viên (MSSV):** 31241021983
- **Lớp chuyên ngành:** Thương mại Điện tử - Khóa 50 (UEH)
- **Repository GitHub:** [https://github.com/anhuynh31241021983-ctrl/BTVN_BUOI2](https://github.com/anhuynh31241021983-ctrl/BTVN_BUOI2)

---

## 1. Giới thiệu bài tập
Bài tập cá nhân Buổi 2 tiếp tục kế thừa và phát triển sản phẩm đã khảo sát và xây dựng từ Buổi 1. Dự án tập trung vào phân khúc **Thương mại điện tử giá trị cao (High-Ticket E-commerce)** với mô hình Showroom & Đặt cọc xe điện trực tuyến VinFast.

Mục tiêu trọng tâm của bài tập Buổi 2:
1. Tái cấu trúc mã nguồn theo chuẩn **HTML5 ngữ nghĩa (Semantic Web)**.
2. Tách biệt hoàn toàn tầng trình bày sang **tệp CSS bên ngoài (`css/style.css`)**.
3. Ứng dụng thành thạo **CSS Box Model**, **CSS Selectors**, **Flexbox** cho hệ thống điều hướng và **CSS Grid** cho danh sách sản phẩm.
4. Tối ưu trải nghiệm tương tác với pseudo-classes (`:hover`, `transition`) và tiêu chuẩn tiếp cận **WCAG A11y** (`:focus-visible`).
5. Thực hành quy trình kiểm thử trên Chrome DevTools, tự sửa lỗi độc lập và làm chủ AI có kiểm soát.

---

## 2. Website tham khảo & Khu vực cải tiến
- **Website tham khảo:** VinFast Auto Vietnam ([https://vinfastauto.com/vn_vi](https://vinfastauto.com/vn_vi)) - Cổng thông tin & đặt cọc ô tô điện trực tuyến chính thức.
- **Khu vực trọng tâm được chọn để cải tiến (theo yêu cầu đề bài):**
  1. **Header & Thanh điều hướng:** Tái cấu trúc bằng `<header>`, `<nav>`, `<ul>`, `<li>`, `<a>` và căn chỉnh dàn hàng ngang linh hoạt bằng **Flexbox**.
  2. **Khu vực Danh sách xe (Showroom Grid):** Bố trí 4 dòng xe tiêu biểu (**VF 3, VF 6, VF 7, VF 9**) dạng lưới đa chiều bằng **CSS Grid**.
  3. **Thẻ sản phẩm xe điện (EV Card):** Chuẩn hóa thẻ `<article>` độc lập, ứng dụng **CSS Box Model** (`padding`, `margin`, `border`, `border-radius`), tích hợp cụm 3 thông số pin cốt lõi và nhóm nút thao tác (Xem chi tiết + Đặt cọc).

---

## 3. Những kỹ thuật HTML5 & CSS3 đã thực hành
1. **HTML5 Semantic:** Sử dụng đúng ngữ nghĩa các phần tử `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>` thay cho việc lạm dụng thẻ `<div>`.
2. **Khả năng tiếp cận & SEO (Accessibility):** 
   - Thêm thuộc tính `alt` mô tả chi tiết kiểu dáng, màu sắc, bối cảnh cho thẻ `<img>`.
   - Bổ sung `aria-label` cho menu và bảng màu, `role="button"` và `tabindex="0"`.
   - Thiết lập trạng thái `:focus-visible` với viền cam tương phản cao phục vụ điều hướng bằng phím `Tab`.
3. **Tổ chức tệp CSS độc lập:** Tách riêng `css/style.css`, liên kết bằng `<link rel="stylesheet">`.
4. **CSS Box Model & Reset:**
   - Sử dụng `* { box-sizing: border-box; }` chuẩn quốc tế để padding và border không làm vỡ kích thước phần tử.
   - Phân định rõ `margin` (khoảng cách bên ngoài thẻ) và `padding` (khoảng đệm bên trong thẻ).
5. **CSS Selector đa dạng:**
   - *Element selector:* `body`, `img`
   - *Class selector:* `.ev-card`, `.btn-deposit`, `.car-img`
   - *Descendant selector:* `.ev-card .car-name`, `.ev-card .price-number`
6. **Flexbox (Bố cục 1 chiều):**
   - Header: `display: flex; justify-content: space-between; align-items: center; gap: 20px;`
   - Menu: `display: flex; gap: 24px; align-items: center; list-style: none;`
   - Cụm nút hành động: `display: flex; gap: 10px; align-items: stretch;`
7. **CSS Grid (Bố cục 2 chiều):**
   - Lưới danh sách xe: `display: grid; grid-template-columns: repeat(4, minmax(0, 1fr)); gap: 24px;`
   - Chống méo hình ảnh xe: `width: 100%; aspect-ratio: 16 / 10; object-fit: cover;`
8. **Hiệu ứng tương tác mượt mà:** Pseudo-class `:hover`, `transform: translateY(-8px)`, `transition: all 0.35s ease`.

---

## 4. Hướng dẫn chạy website
1. **Cách 1 (Mở trực tiếp):** Tải repository về máy, giải nén và nhấp đúp vào file `index.html` để mở trên Google Chrome, Edge hoặc Firefox.
2. **Cách 2 (Sử dụng VS Code Live Server):**
   - Mở thư mục `BTVN_BUOI2` trong Visual Studio Code.
   - Cài đặt tiện ích mở rộng **Live Server** (nếu chưa có).
   - Nhấp chuột phải vào `index.html` chọn **"Open with Live Server"** (phím tắt `Alt + L, Alt + O`).
   - Website sẽ chạy cục bộ tại: `http://127.0.0.1:5500/index.html`.

---

## 5. Những thay đổi đã thực hiện (So sánh Trước và Sau)

| Tiêu chí | Trước khi cải thiện (Buổi 1) | Sau khi cải thiện (Buổi 2) |
| :--- | :--- | :--- |
| **Menu điều hướng** | Dùng các thẻ `<span>` vô nghĩa, các liên kết không có thẻ `<a>`, không chuẩn danh sách `<ul>/<li>`. | Tái cấu trúc chuẩn HTML5: `<nav>` chứa `<ul class="nav-list"><li><a class="nav-item"></a></li></ul>`. |
| **Thao tác hành động** | Thẻ xe chỉ có duy nhất 1 nút đặt cọc, thiếu nút dẫn đến trang chi tiết thông số xe. | Bổ sung cụm 2 nút bằng Flexbox: Nút liên kết `<a class="btn-detail">Xem chi tiết</a>` song song nút `<button class="btn-deposit">Đặt cọc</button>`. |
| **Trải nghiệm tiếp cận (A11y)** | Chưa có trạng thái `:focus-visible`, người dùng phím Tab không biết đang chọn phần tử nào. | Bổ sung `:focus-visible` với đường viền `outline: 3px solid #f59e0b; outline-offset: 3px;` chuẩn WCAG. |
| **Tỉ lệ hình ảnh** | Dùng `padding-top: 62%` kiểu cũ, dễ gây sai lệch trên các trình duyệt mới. | Nâng cấp thuộc tính CSS hiện đại `aspect-ratio: 16 / 10; object-fit: cover;` chống hoàn toàn méo hình. |
| **Thẻ sản phẩm (Box Model)** | Chiều cao các thẻ có thể lệch nhẹ khi tên xe dài; nút bấm bị so le đáy. | Chuẩn hóa Box Model: `padding: 22px;`, cố định chiều cao tên xe 2 dòng, gán `margin-top: auto` cho khối nút để mọi nút luôn thẳng hàng sát đáy. |

---

## 6. Báo cáo kiểm thử giao diện & Tự sửa lỗi độc lập (Bước 8)

### 6.1. Bảng kiểm thử (Checklist 7 tiêu chí)
| STT | Nội dung kiểm tra | Kết quả | Ghi chú thực tế |
| :-: | :--- | :---: | :--- |
| 1 | Trang HTML mở được bình thường | **Đạt** | Tải mượt mà, cấu trúc DOM phân cấp rõ ràng. |
| 2 | CSS được áp dụng chính xác | **Đạt** | Nạp file `css/style.css` thành công, mã trạng thái HTTP 200. |
| 3 | Hình ảnh hiển thị đúng & không méo | **Đạt** | Tỉ lệ xe 16:10 sắc nét, không bị dãn dọc hay bẹp ngang nhờ `object-fit: cover`. |
| 4 | Liên kết hoạt động | **Đạt** | Các liên kết nhảy mượt đến `#showroom`, `#hero`, và liên kết chi tiết xe. |
| 5 | Bố cục không bị tràn màn hình | **Đạt** | Kiểm tra DevTools tại 1366px (4 cột), 768px (2 cột) và 390px (1 cột) không có thanh cuộn ngang. |
| 6 | Hover / Focus-visible hoạt động | **Đạt** | Rê chuột nhấc thẻ xe và sáng viền; bấm phím Tab hiện viền cam rõ ràng. |
| 7 | Đã tự sửa ít nhất 1 vấn đề độc lập | **Đạt** | Đã sửa hiện tượng nút đặt cọc bị lệch hàng ngang khi tên dòng xe có độ dài khác nhau. |

### 6.2. Báo cáo vấn đề tự phát hiện & cách khắc phục độc lập
- **Vấn đề phát hiện:** Dòng xe VF 9 có tên dài (*"VinFast VF 9 Plus - Ghế Cơ Trưởng Thương Gia"*) dài hơn dòng VF 3 (*"VinFast VF 3 - Phong Cách Sáng Tạo"*). Điều này làm phần thân thẻ xe VF 9 dài hơn, đẩy nút bấm của các xe trên cùng một hàng bị so le, mất cân đối thị giác.
- **Nguyên nhân kỹ thuật:** Thẻ cha `.ev-card` chưa có cơ chế ép phần tử con cuối cùng tự neo về đáy khi chiều cao linh hoạt.
- **Cách khắc phục độc lập của sinh viên:**
  1. Thêm quy tắc khống chế chiều cao cho tiêu đề xe:
     ```css
     .ev-card .car-name {
         display: -webkit-box;
         -webkit-line-clamp: 2;
         -webkit-box-orient: vertical;
         overflow: hidden;
         height: 46px;
     }
     ```
  2. Áp dụng kỹ thuật Flexbox auto margin cho khối nút thao tác:
     ```css
     .card-action {
         margin-top: auto; /* Tự động hấp thụ toàn bộ khoảng trống còn thừa để đẩy nút sát đáy */
     }
     ```
- **Kết quả:** Trên mọi kích thước màn hình, toàn bộ các nút bấm của cả 4 thẻ xe đều thẳng tắp theo một đường chân trời hoàn hảo.

---

## 7. Trả lời 7 câu hỏi kiểm tra kiến thức (Mục 12)

### Câu 1: Trong khu vực giao diện của em, em đã sử dụng những phần tử HTML5 nào? Vì sao em chọn chúng?
- **Trả lời:**
  - Em sử dụng:
    + `<header>` và `<nav>`: Định nghĩa khu vực đầu trang và thanh điều hướng chính của VinFast.
    + `<main>`: Bao bọc khu vực nội dung trọng tâm duy nhất của trang (Showroom xe điện).
    + `<section>`: Chia các khối nội dung lớn có tiêu đề độc lập (`.hero-banner` và `.ev-showroom`).
    + `<article>`: Đại diện cho mỗi thẻ xe điện (`.ev-card`).
    + `<footer>`: Chứa thông tin pháp lý, bản quyền và chính sách thanh toán bảo mật.
  - **Lý do chọn:** Các thẻ semantic giúp trình duyệt, bộ máy tìm kiếm (SEO) và công cụ đọc màn hình (Screen Reader) hiểu chính xác ý nghĩa và phân cấp dữ liệu của trang thương mại điện tử, thay vì chỉ là các thẻ `<div>` vô nghĩa.

### Câu 2: Giải thích sự khác nhau giữa margin và padding. Cho ví dụ từ thẻ sản phẩm của em.
- **Trả lời:**
  - **Padding (Vùng đệm trong):** Nằm bên trong đường viền (border), giữa nội dung và viền của phần tử. Padding mang màu nền của phần tử đó.
  - **Margin (Vùng lề ngoài):** Nằm bên ngoài đường viền (border), dùng để tạo khoảng cách giữa phần tử này với phần tử khác. Margin hoàn toàn trong suốt.
- **Ví dụ từ thẻ `.ev-card` của em:**
  - `padding: 22px;` trong `.card-body`: Tạo khoảng cách 22px đệm xung quanh chữ, giá tiền và thông số pin, giúp nội dung không bị dính sát vào đường viền kính mờ.
  - `margin: 0;` ở `.ev-card` (kết hợp với `gap: 24px;` của lưới Grid cha): Đảm bảo 4 thẻ xe đứng cách nhau 24px đều đặn, không bị chạm vào nhau.

### Câu 3: Trong bài của em, Flexbox được sử dụng ở đâu? Giải thích tác dụng của justify-content và align-items.
- **Trả lời:**
  - **Nơi sử dụng Flexbox:** 
    1. Thanh header `.header-wrap`: Căn Logo sang trái và Menu sang phải.
    2. Danh sách menu `.nav-links .nav-list`: Căn các mục menu theo hàng ngang.
    3. Nhóm nút thao tác `.action-buttons-group`: Căn nút "Xem chi tiết" và nút "Đặt cọc".
  - **Tác dụng của các thuộc tính:**
    - `justify-content`: Căn chỉnh các phần tử con theo **trục chính (Main Axis)**. Em dùng `justify-content: space-between;` để đẩy cụm Logo và cụm Menu dạt về hai cực đối diện của thanh header.
    - `align-items`: Căn chỉnh các phần tử con theo **trục phụ (Cross Axis)** vuông góc với trục chính. Em dùng `align-items: center;` để Logo và Menu luôn nằm chính giữa theo phương thẳng đứng.

### Câu 4: CSS Grid khác Flexbox như thế nào? Vì sao em sử dụng Grid cho danh sách sản phẩm?
- **Trả lời:**
  - **Khác biệt cốt lõi:**
    - **Flexbox là hệ thống bố cục 1 chiều (1D):** Chỉ tối ưu khi sắp xếp các phần tử theo hàng *hoặc* theo cột (thanh điều hướng, nhóm icon, nút bấm).
    - **CSS Grid là hệ thống bố cục 2 chiều (2D):** Cho phép kiểm soát đồng thời cả **hàng (row) và cột (column)** cùng lúc.
  - **Lý do dùng Grid cho danh sách sản phẩm:** Danh sách xe điện của VinFast cần hiển thị thành lưới 4 cột trên Desktop và co về 2 cột trên Tablet. CSS Grid cho phép định nghĩa số cột chính xác qua `grid-template-columns: repeat(4, minmax(0, 1fr));` và kiểm soát khoảng cách bằng `gap: 24px;` một cách ngắn gọn, không lo bị vỡ dòng so với việc float hay flexbox thủ công.

### Câu 5: Nếu xóa quy tắc CSS `display: grid` khỏi danh sách sản phẩm, giao diện có thể thay đổi như thế nào?
- **Trả lời:**
  - Phần tử cha `.ev-grid` vốn là thẻ `<div>` mang thuộc tính khối mặc định (`display: block`).
  - Nếu xóa bỏ `display: grid`, các thẻ con `<article class="ev-card">` sẽ trở lại dòng chảy tự nhiên (normal flow) của phần tử block: **chiếm trọn 100% chiều rộng màn hình và xếp chồng dọc từ trên xuống dưới**.
  - Lưới 4 cột ngang sẽ biến mất hoàn toàn, 4 chiếc xe hiển thị nối tiếp nhau tạo thành một trang cuộn rất dài và phá vỡ bố cục đối chiếu so sánh của showroom.

### Câu 6: Vì sao cần sử dụng thuộc tính `alt` cho hình ảnh sản phẩm?
- **Trả lời:** Thuộc tính `alt` (Alternative Text) tối quan trọng vì 3 lý do:
  1. **Khả năng tiếp cận (Accessibility - WCAG):** Thiết bị đọc màn hình (Screen Reader) sẽ đọc văn bản trong `alt` (ví dụ: *"Xe điện VinFast VF 7 màu đỏ Crimson phong cách thể thao phi đối xứng"*) giúp người khiếm thị hình dung được mẫu xe.
  2. **Dự phòng khi lỗi mạng (Fallback UX):** Nếu đường truyền mạng chập chờn hoặc link ảnh bị lỗi, người dùng vẫn đọc được dòng chữ mô tả thay vì nhìn thấy biểu tượng ảnh vỡ.
  3. **Tối ưu hóa SEO TMĐT:** Google Bot không thể "nhìn" ảnh như con người mà dựa vào thẻ `alt` để hiểu ngữ cảnh, giúp hình ảnh xe của website xuất hiện trên trang kết quả tìm kiếm Google Hình ảnh.

### Câu 7: Hãy nêu một đề xuất của AI mà em đã kiểm tra hoặc điều chỉnh trước khi đưa vào bài tập.
- **Trả lời thực tế:**
  - **Đề xuất ban đầu của AI:** Khi em nhờ AI phân chia lưới sản phẩm, AI gợi ý dùng thư viện bên ngoài (Bootstrap grid) và tự động tạo thêm một dòng xe giả định mang tên "VinFast VF 2".
  - **Kiểm tra & điều chỉnh của em:**
    - Thứ nhất: Đề bài của Thầy Tuấn nghiêm cấm dùng Bootstrap hay Tailwind, em đã yêu cầu viết bằng **CSS Grid thuần** với cú pháp `repeat(4, minmax(0, 1fr))`.
    - Thứ hai: Em đối chiếu trực tiếp dữ liệu từ cổng thông tin VinFast chính thức `vinfastauto.com/vn_vi`, loại bỏ hoàn toàn dòng xe ảo "VF 2", chuẩn hóa lại bộ 4 dòng xe chiến lược có thật: **VF 3 (Mini SUV), VF 6 (B-SUV), VF 7 (C-SUV), VF 9 (E-SUV)** với thông số pin (km/sạc, thời gian sạc, công suất HP) và giá cọc chính xác 100%.

---

## 8. Sẵn sàng cho yêu cầu sửa mã trực tiếp của Giảng viên (Mục 13)

| Yêu cầu của Giảng viên | File cần mở | Thao tác can thiệp nhanh |
| :--- | :---: | :--- |
| **Đổi màu giá sản phẩm** | `css/style.css` | Tìm `.ev-card .price-number`, đổi `color: #ffffff;` thành `color: #f59e0b;` (vàng kim) hoặc `#38bdf8;` (xanh điện). |
| **Thay đổi số cột của danh sách xe** | `css/style.css` | Tìm `.ev-grid`, đổi `repeat(4, minmax(0, 1fr))` thành `repeat(3, minmax(0, 1fr))` (3 cột) hoặc `repeat(2, minmax(0, 1fr))` (2 cột). |
| **Thay đổi khoảng cách đệm bên trong thẻ (Padding)** | `css/style.css` | Tìm `.card-body`, đổi `padding: 22px;` thành `padding: 30px;` (thoáng hơn) hoặc `14px;` (gọn lại). |
| **Điều chỉnh khoảng cách menu** | `css/style.css` | Tìm `.nav-links .nav-list`, đổi `gap: 24px;` thành `gap: 36px;`. |
| **Sửa hoặc thêm thuộc tính `alt`** | `index.html` | Tìm thẻ `<img class="car-img">`, cập nhật nội dung văn bản trong thuộc tính `alt="..."`. |

---

## 9. Cập nhật và triển khai lên GitHub
Mã nguồn đã được commit và push lên nhánh `main` của repository GitHub:
```bash
git add .
git commit -m "Practice HTML5 semantics, CSS Box Model, Flexbox and Grid - Buoi 2 UEH"
git push origin main
```
URL: [https://github.com/anhuynh31241021983-ctrl/BTVN_BUOI2](https://github.com/anhuynh31241021983-ctrl/BTVN_BUOI2)
