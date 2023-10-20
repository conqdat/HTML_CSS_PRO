# HTML_CSS_PRO_F8

- **Sử dụng CSS Prefix (tiền tố trong CSS) cho một số thuộc tính CSS có thể hoạt động trên nhiều trình duyệt hơn. Các tiền tố thường sử dụng bao gồm: -webkit-, -moz-, -ms-, -o-, bạn có thể tham khảo thêm tại: Vendor Prefix.**

- **Cách đơn giản nhất để thêm CSS Prefix thủ công đó là: trước tiên hãy viết CSS không có prefix, sau đó sử dụng trang web autoprefixer.github.io và dán (paste) CSS của bạn vào để nhận lại CSS có đầy đủ prefix.**

- **Các thuộc tính CSS có nhãn user agent stylesheet là thuộc tính mặc định được trình duyệt tự động thêm vào. Bạn có thể kiểm tra được điều này thông qua DevTools.**

- **Chỉ các thuộc tính CSS có thông số Inherited: yes mới có tính thừa kế. Có thể tra cứu các thuộc tính CSS tại w3schools.com hoặc developer.mozilla.org với từ khóa tìm kiếm: CSS [tên thuộc tính] property.**

- **Tất cả các thẻ HTML mặc định có thuộc tính display, tùy vào loại thẻ đó thì display sẽ có giá trị tương ứng. Ví dụ: thẻ block sẽ mặc định có display: block, thẻ inline sẽ mặc định có display: inline.**

## Trường hợp sử dụng display: none, opacity: 0 và visibility: hidden: ( chương 15 )

### display: none

- Ẩn và loại bỏ không gian/diện tích của phần tử khỏi bố cục trang web
- Không cần hiệu ứng chuyển tiếp (transition)

### opacity: 0

- Tăng/giảm độ mờ của phần tử HTML trên giao diện trang web
- Kết hợp với transition để tạo hiệu ứng chuyển tiếp như: fade in, fade out

### visibility: hidden

- Ẩn phần tử mà không làm thay đổi bố cục trang web (không gian của phần tử không bị loại bỏ)
- Kết hợp với transition và opacity để tạo hiệu ứng chuyển tiếp như: fade in, fade out

## CSS Selector:

- `*` : Chọn tất cả các phần tử
- `element` : Chọn tất cả các phần tử có tên là element
- `.class` : Chọn tất cả các phần tử có class là class
- `#id` : Chọn tất cả các phần tử có id là id
- `element.class` : Chọn tất cả các phần tử có tên là element **và** class là class
- `element, element` : Chọn tất cả các phần tử có tên là element **hoặc** element
- `element element` : Chọn tất cả các phần tử có tên là element **nằm trong** element
- `element > element` : Chọn tất cả các phần tử có tên là element **là con trực tiếp của** element
- `element + element` : Chọn tất cả các phần tử có tên là element **là anh em kế tiếp của** element
- `element ~ element` : Chọn tất cả các phần tử có tên là element **là anh em của** element
- `[attribute]` : Chọn tất cả các phần tử có attribute
- `[attribute=value]` : Chọn tất cả các phần tử có attribute và giá trị của attribute là value
- `[attribute~=value]` : Chọn tất cả các phần tử có attribute và giá trị của attribute là value (có khoảng trắng)
- `[attribute|=value]` : Chọn tất cả các phần tử có attribute và giá trị của attribute là value (có dấu gạch ngang)
- `[attribute^=value]` : Chọn tất cả các phần tử có attribute và giá trị của attribute bắt đầu bằng value
- `[attribute$=value]` : Chọn tất cả các phần tử có attribute và giá trị của attribute kết thúc bằng value
- `[attribute*=value]` : Chọn tất cả các phần tử có attribute và giá trị của attribute chứa value
- `:link` : Chọn tất cả các phần tử là link chưa được truy cập
- `:visited` : Chọn tất cả các phần tử là link đã được truy cập
- `:active` : Chọn tất cả các phần tử đang được click
- `:hover` : Chọn tất cả các phần tử đang được hover
- `:focus` : Chọn tất cả các phần tử đang được focus
- `:first-letter` : Chọn tất cả các chữ cái đầu tiên của phần tử
- `:first-line` : Chọn tất cả các dòng đầu tiên của phần tử
- `:first-child` : Chọn tất cả các phần tử là con đầu tiên của phần tử cha
- `:before` : Chọn tất cả các phần tử trước phần tử
- `:after` : Chọn tất cả các phần tử sau phần tử
- `:lang(language)` : Chọn tất cả các phần tử có ngôn ngữ là language
- `:first-of-type` : Chọn tất cả các phần tử là con đầu tiên của phần tử cha có cùng tên
- `:last-of-type` : Chọn tất cả các phần tử là con cuối cùng của phần tử cha có cùng tên

## [Độ ưu tiên của CSC](https://www.w3schools.com/css/css_specificity.asp):

- Inline styles - Example: `<h1 style="color: pink;">`
- IDs - Example: #navbar
- Classes, pseudo-classes, attribute selectors - Example: .test, :hover, [href]
- Elements and pseudo-elements - Example: h1, ::before

## Box model: Margin > Border > Padding > Content

### Padding:

- Padding là phần không gian được đệm vào xung quanh nội dung của phần tử giúp phần tử đó trở nên dày hơn. Trong Box Model, padding nằm ở vị trí thứ 2 tính từ trong ra ngoài, nằm giữa content và border của phần tử.

  > padding: 10px; /_ Đệm cả 4 hướng 10px
  > padding: 10px 20px; /_ Đệm trên/dưới 10px, trái/phải 20px _/
  > padding: 10px 20px 30px; /_ Đệm trên 10px, trái/phải 20px, dưới 30px _/
  > padding: 10px 20px 30px 40px; /_ Đệm theo thứ tự: trên-phải-dưới-trái \*/

- Trường hợp sử dụng:
  - Làm button
  - Khoảng cách nội dụng với Header, Footer, Sidebar, Content

### Border: Làm tăng kích thước phần tử, không chiếm k gian

- Trường hợp sử dụng:
  - Màu nền/ảnh nền được đổ từ border vào trong
  - Boder-radius: Làm tròn góc

### Outline: Làm tăng kích thước phần tử, về chiếm không gian, chiều cao

### Margin: không làm thay đổi kích thước phần tử

- Căng giữa bằng margin-left, margin-right => auto ( dùng cho display: block )
- margin-left: auto; => Căng phải ( dùng cho display: block )
- margin-right: auto; => Căng trái ( dùng cho display: block )

#### Margin collapse: Top and bottom margins of elements are sometimes collapsed into a single margin that is equal to the largest of the two margins.

- Các thẻ con liền kề nhau sẽ bị margin collapse. Khắc phục bằng cách float left và width.
- display flex

## Box sizing:

- content-box: default
- border-box: padding + border + content

## CSS Units

### Absolute units: **px**, cm, mm, in, pt, pc

- Hiển thị cố định và không thể linh hoạt trên các thiết bị khác nhau

### Relative units: %, em, rem, vw, vh, vmin, vmax

- %: **phụ thuộc vào thẻ cha**
- vh: chiều cao của viewport
- vw: chiều rộng của viewport
- **em: phụ thuộc vào font-size của thẻ cha**
- **rem: phụ thuộc vào font-size của thẻ root ( thẻ html )**

## Color in CSS:

- name: red, green,...
- HEX: #ff0000, #00ff00,... // 0123456789abcdef // #rrggbb
- RGB / RGBA: rgb(255, 0, 0), rgba(255, 0, 0, 0.5)
- currentColor: color: red; border: 1px solid currentColor;

## Background:

- Background-color:
- Background-image:
  - Default Value: none
  - Background-repeat: repeat, repeat-x, repeat-y, no-repeat
  - Background-position: top left, top center, top right, center left, center center, center right, bottom left, bottom center, bottom right
  - Background-attachment: scroll, fixed, local
  - Background-size: auto, cover (lắp đầy), contain (chứa)
  - Linear-gradient: background-image: linear-gradient(to right, red, yellow);

## Font:

- Serif: có chân
- Sans-serif: không chân ( được sử dụng rất nhiều )
- Monospace: đều nhau ( viết code )
- Letter-spacing: Khoảng cách giữa các chữ cái
- Word-spacing: Khoảng cách giữa các từ
- Line-height: Khoảng cách giữa các dòng
- Text-align: left, right, center, justify
- Text-decoration: none, underline, overline, line-through

## Image

- Độ rộng tối đa: max-width: 100%;
- Lazy load: Ảnh được load khi nào cần thiết => <img loading="lazy" />
- Xử lý hình ảnh có kích thước tối đa: max-with: 100%;
- Giữ đúng tỉ lệ hình ảnh: đặt with or height

## Position:

- Static: default
- Relative: tương đối với vị trí ban đầu
- Absolute: - định vị theo thẻ body nếu không có thẻ nào có position: relative - tương đối với thẻ cha có position: relative - có nhiều thẻ có position: absolute thì thẻ nào viết sau thì thẻ đó nằm trên cùng
<!-- - Fixed: tương đối với viewport  -->

## Responsive

### Thẻ meta viewport

### media queries

### Breakpoints

/_ PC breakpoint _/
@media screen and (min-width: 992px) {
.pc {
display: block;
}
}

/_ Tablet breakpoint _/
@media screen and (min-width: 768px) and (max-width: 991.98px) {
.tablet {
display: block;
}
}

/_ Mobile breakpoint _/
@media screen and (max-width: 767.98px) {
.mobile {
display: block;
}
}

## Gird system


## SASS / CSCC
- sass scss/scss.scss css/scss.css -w
- Nested rules và variables trong Sass
- &: parent
- Biến: $primary / Usage: color: $primary-color;