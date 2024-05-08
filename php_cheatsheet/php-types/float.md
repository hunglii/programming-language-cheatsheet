# Kiểu số thực

Kiểu số thực kí hiệu là `float`, các số được viết dưới dạng dấu chấm động:

```php
<?php
var_dump(1.25); // float(1.25)
var_dump(-0.1); // float(-0.1)
var_dump(1_234_567.89); // float(1234567.89)
var_dump(0.12E1); // float(1.2)
```

Biểu diễn số thực dưới dạng `float` là một biểu diễn gần đúng:

```php
// 0.1 + 0.1 + 0.1 = 0.299999999999...
$total = 0.1 + 0.1 + 0.1;

// kiểm tra xem $total có bằng 0.3 hay không
var_dump($total == 0.3); // bool(false)
```

Hàm `is_float()` hoặc `is_real()` kiểm tra một giá trị có phải số thực không:

```php
var_dump(is_float(0.5)); // bool(true)
```
