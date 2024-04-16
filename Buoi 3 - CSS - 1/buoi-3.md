# CSS (Cascading Style Sheets)

## 1. CSS là gì? CSS giúp gì trong việc code Web App ?
CSS là ngôn ngữ tạo phong cách cho trang web. Nó dùng để tạo phong cách và định kiểu cho những yếu tố được viết dưới dạng ngôn ngữ đánh dấu, như là HTML. CSS giúp kiểm soát cách các phần tử HTML hiển thị trên trang, bao gồm màu sắc, kích thước, font chữ, khoảng cách, và nhiều thuộc tính khác.

### Một số cách mà CSS hỗ trợ trong việc code Web App:
- **Định dạng và trang trí giao diện người dùng:** CSS cho phép bạn thiết lập các thuộc tính như màu sắc, kích thước, font chữ, độ trong suốt và nhiều thuộc tính khác để tạo ra giao diện người dùng đẹp mắt và dễ sử dụng.
- **Responsive Design:** CSS cung cấp các kỹ thuật để tạo ra giao diện web linh hoạt, tự động điều chỉnh dựa trên kích thước màn hình. Điều này giúp tối ưu hóa trải nghiệm người dùng trên nhiều thiết bị, từ máy tính đến điện thoại di động.
- **Kiểm soát bố cục (Layout):** CSS cho phép bạn kiểm soát cách các phần tử HTML hiển thị và sắp xếp trên trang. Bạn có thể sử dụng các thuộc tính như display, position, float để quyết định vị trí và kích thước của các phần tử.
- **Hiệu ứng và chuyển động:** CSS3 cung cấp nhiều tính năng mới, như animation và transition, giúp tạo ra các hiệu ứng và chuyển động mượt mà trên trang web mà không cần sử dụng JavaScript.
- **Quản lý kiểu dáng trang web:** CSS cho phép bạn tách biệt kiểu dáng (style) từ nội dung (content) và cấu trúc (structure) của trang web. Điều này giúp bảo trì và quản lý mã nguồn dễ dàng hơn.
- **Tối ưu hóa hiệu suất:** Bằng cách sử dụng CSS, bạn có thể tối ưu hóa hiệu suất trang web bằng cách giảm kích thước tập tin và tối ưu hóa các thuộc tính, giúp trang web tải nhanh hơn và có trải nghiệm người dùng tốt hơn.
## 2. Cách nhúng CSS vào website:
Để CSS có thể thực thi trên website hoặc HTML Documents thì phải tiến hành nhúng CSS vào website. Nếu không, các định dạng CSS sẽ không thực thi trên HTML. Có 3 cách nhúng CSS vào website:
- **Inline CSS** – Nhúng trực tiếp vào tài liệu HTML thông qua thuộc tính style.
``` html
<p style="color:blue">This is a paragraph.</p>
```
- **Internal CSS** – dùng thẻ `<style>` bên trong thẻ `<head>` của HTML để tạo ra nơi viết mã CSS.
``` html 
<head>
  <style>
    p {
      color: blue;
    }
  </style>
</head>
```
- **External CSS** – Tạo một tập tin .css riêng và nhúng vào tài liệu HTML thông qua cặp thẻ `<link>`.
``` html
<head>
  <link rel="stylesheet" type="text/css" href="style.css">
</head>
```
## 3. Kiến thức đường dẫn quan trọng cần nắm: ./ và ../
### **`./`** (Đường dẫn tương đối hiện tại):

- **`./`** đại diện cho thư mục hiện tại, nghĩa là nó chỉ đến tệp tin hoặc thư mục trong thư mục mà bạn đang làm việc. Khi bạn sử dụng **`./`**, bạn cho hệ thống biết rằng bạn muốn trỏ đến một tệp tin hoặc thư mục ở trong thư mục hiện tại.
Ví dụ: Nếu bạn đang ở trong thư mục "images" và muốn truy cập tệp tin "logo.jpg" trong thư mục hiện tại, bạn có thể sử dụng đường dẫn: ./logo.jpg.
### **`../`** (Đường dẫn tương đối thư mục cha): 
- **`../`** đại diện cho thư mục cha của thư mục hiện tại. Khi bạn sử dụng **`../`**, bạn đang cho hệ thống biết rằng bạn muốn truy cập một tệp tin hoặc thư mục ở trong thư mục cha của thư mục hiện tại.
- Ví dụ: Nếu bạn đang ở trong thư mục "css" và muốn truy cập tệp tin **`"style.css"`** trong thư mục cha, bạn có thể sử dụng đường dẫn: **`../style.css`**.

## 4. Selectors là gì ? trong CSS có những loại **selector** nào?
Trong CSS (Cascading Style Sheets), "selectors" là phần của mã CSS được sử dụng để xác định các phần tử HTML mà bạn muốn áp dụng các quy tắc định dạng. Selectors giúp bạn chọn các phần tử cụ thể hoặc nhóm các phần tử để áp dụng các kiểu dáng và trang trí.

### Selector phần tử (Element Selector):
``` css
p {
  color: blue;
}
```
Áp dụng kiểu dáng cho tất cả các phần tử `<p>` trong trang.
### Selector lớp (Class Selector):
``` css
.highlight {
  background-color: yellow;
}
```
Áp dụng kiểu dáng cho tất cả các phần tử có class là "highlight".
### Selector ID (ID Selector):
``` css
#header {
  font-size: 24px;
}
```
Áp dụng kiểu dáng cho phần tử có id là "header".
### Selector kết hợp (Combination Selector):
``` css
h2.title {
  color: red;
}
```
Áp dụng kiểu dáng cho tất cả các phần tử `<h2>` có class là "title".
## 5. Hiểu rõ về độ ưu tiên trong CSS:
### - Internal, External:
- không có sự ưu tiên hơn cái nào chỉ đơn giản là cái nào viết sau cái nào.
- ví dụ:
```html
<head>
  <link href="style.css">
  <style>
    .selector{
      ...
    }
  </style>
</head>
```
### - Inline - 4
### - #id - 3
### - .class - 2
### - tag - 1
### - Equal specificity?
Có thể hiểu là thằng nào được khai báo sau cùng sẽ được ưu tiên
``` css
#myElement {
    color: green;
}
#myElement {
    color: yellow; 
}
```
### - Universal selector and inherited?
Các phần tử con sẽ được thừa hưởng từ phần tử cha
``` css
html{
  color: red;
}
h1{
  color: red
}
```
### - importance

## 6. Các thuộc tính cơ bản (dể hiểu):
- **`color`**: màu chữ.
- **`font-size`**: kích thước chữ.
- **`font-weight`**: độ đậm chữ.
- **`font-style`**: kiểu font của văn bản.
- **`text-decoration`**: định dạng trang trí cho văn bản.
- **`letter-spacing`**: khoảng cách giữa các ký tự trong một đoạn văn bản.
- **`word-spacing`**: xác định khoảng cách giữa các từ trong một đoạn văn bản.
- **`line-height`**: khoảng cách giữa từ và chiều cao dòng trong văn bản.
- **`width`**: chiều rộng phần tử.
- **`height`**: chiều cao phần tử.
- **`border-radius`**: xác định độ cong của các góc của một phần tử.