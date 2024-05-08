# Kiểu số nguyên

Kiểu số nguyên kí hiệu là `int` và có các giá trị như `-3, -2, -1, 0, 1, 2, 3,...`.

Lấy thông tin về kiểu số nguyên:

```php
# kích thước (tính theo byte)
echo PHP_INT_SIZE; // 8

# giá trị nhỏ nhất
echo PHP_INT_MIN; // -9223372036854775808

# giá trị lớn nhất
echo PHP_INT_MAX; // 9223372036854775807
```

PHP có thể biểu diễn các số nguyên theo hệ thập phân, bát phân, nhị phân và thập lục phân:

```php
# số nguyên hệ thập phân
var_dump(2000); // int(2000)
var_dump(-100); // int(-100)
var_dump(1_000_000); // int(1000000)

/*
    Số nguyên hệ bát phân bắt đầu bằng tiền tố 0,
    theo sau là các chữ số từ 0 đến 7
*/
var_dump(011); // int(9)
var_dump(-010); // int(-8)

/*
    Số nguyên hệ nhị phân, bắt đầu bởi tiền tố 0b,
    theo sau là các chữ số 0 và 1
*/
var_dump(0b1011); // int(11)
var_dump(-0b11); // int(-3)

/*
    Số nguyên hệ thập lục phân, bắt đầu bởi tiền tố 0x,
    theo sau là các chữ số từ 0 đến 9,
    các chữ cái từ A đến F
*/
var_dump(0x1FA2); // int(8098)
var_dump(-0xFF); // int(-255)
```

Hàm `is_int()` kiểm tra xem một giá trị có phải số nguyên không, là số nguyên thì trả về `true`, không là số nguyên thì trả về `false`.

```php
<?php
$amount = 100;
var_dump(is_int($amount)); // bool(true)
echo is_int($amount); // 1
```
