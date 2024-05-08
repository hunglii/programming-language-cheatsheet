# Kiểu lôgic

Kiểu lôgic kí hiệu là `bool` chỉ có hai giá trị `true` và `false`.

```php
<?php
$is_submitted = true;
$is_email_valid = false;

var_dump($is_submitted); // bool(true)
var_dump($is_email_valid); // bool(false)

echo $is_submitted; // 1
echo $is_email_valid; // không hiển thị gì
```

Hàm `is_bool()` kiểm tra xem một giá trị có kiểu lôgic không:

```php
$is_email_valid = false;
var_dump(is_bool($is_email_valid)); // bool(true)
echo is_bool($is_email_valid); // hiển thị 1

$text = 'a string';
var_dump(is_bool($text)); // bool(false)
echo is_bool($text); // không hiển thị gì
```

Khi sử dụng các giá trị không có kiểu lôgic trong ngữ cảnh cần một giá trị lôgic, PHP chuyển các giá trị này thành giá trị lôgic. Các giá trị sau được chuyển thành `false`:
- Số nguyên không: `0`
- Số thực không: `0.0`
- Chuỗi chứa số 0: `"0"`
- Chuỗi trống: `''` hoặc `""`
- Giá trị `null`
- Mảng trống (mảng không có phần tử)

Các giá trị khác được chuyển thành `true`.