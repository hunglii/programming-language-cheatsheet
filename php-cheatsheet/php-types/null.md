# Kiểu null

Kiểu `null` là một kiểu đặc biệt trong PHP, nó chỉ có một giá trị duy nhất là `null`. Giá trị `null` biểu thị cho sự thiếu vắng giá trị cho một biến.

```php
# khởi tạo biến nhưng chưa có giá trị cụ thể thì gán cho nó giá trị null
$email = null;
var_dump($email); // NULL

# khi gỡ giá trị khỏi biến bằng unset, biến ấy mặc định mang giá trị null
$email = 'webmaster@php.net';
unset($email);

var_dump($email); // NULL
```

Để kiểm tra một giá trị có phải `null` không, dùng hàm `is_null()`:

```php
$email = null;
var_dump(is_null($email)); // bool(true)

$home = 'php.net';
var_dump(is_null($home)); // bool(false)
```

Ngoài ra có thể dùng toán tử so sánh đồng nhất `===` (ba dấu bằng) để kiểm tra một giá trị có là `null` không:

```php
$email = null;
$result = ($email === null);
var_dump($result); // bool(true)

$home = 'php.net';
$result = ($home === null);
var_dump($result); // bool(false)
```
