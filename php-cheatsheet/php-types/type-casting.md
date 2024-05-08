# Chuyển đổi kiểu

## Chuyển đổi sang số nguyên

```php
<?php
# số thực -> số nguyên
var_dump((int)12.5); // int(12)
var_dump((int)12.9); // int(12)
var_dump((int)-12.9); // int(-12)

# chuỗi -> số nguyên
var_dump((int)'Hello'); // int(0)
var_dump((int)'100'); // int(100)
var_dump((int)'100 USD'); // int(100)

# null -> số nguyên
var_dump((int)null); // int(0)

# lôgic -> số nguyên
var_dump((int)true); // int(1)
var_dump((int)false); // int(0)
```

## Chuyển đổi sang số thực

```php
<?php
# số nguyên -> số thực
var_dump((float)100); // float(100)

# chuỗi -> số thực
var_dump((float)'Hello'); // float(0)
var_dump((float)'10'); // float(10)
var_dump((float)'10 USD'); // float(10)
var_dump((float)'-3.2'); // float(-3.2)
var_dump((float)'0.123E3'); // float(123)

# null -> số thực
var_dump((float)null); // float(0)

# lôgic -> số thực
var_dump((float)true); // float(1)
var_dump((float)false); // float(0)
```

## Chuyển đổi sang chuỗi

```php
<?php
# số -> chuỗi
var_dump((string)-1234); // string(5) "-1234"
var_dump((string)0.123E3); // string(3) "123"

# lôgic -> chuỗi
var_dump((string)true); // string(1) "1"
var_dump((string)false); // string(0) ""

# null -> chuỗi
var_dump((string)null); // string(0) ""

# mảng -> chuỗi
var_dump((string)[1,2,3]); // string(5) "Array"
```

Chuyển đổi sang chuỗi được thực hiện ngầm định khi sử dụng toán tử nối `.` hoặc lệnh `echo`...

Trong ví dụ dưới, `$amount` trước tiên được chuyển thành chuỗi `'100'` sau đó chuỗi này được nối với chuỗi `' USD'`:

```php
<?php
$amount = 100;
var_dump($amount . ' USD'); // string(7) "100 USD"
```

Trong ví dụ tiếp theo dưới đây, `true` và `false` trước tiên được chuyển thành chuỗi:

- `true` chuyển thành `"1"`
- `false` chuyển thành chuỗi trống `""`.

Sau đó `echo` hiển thị những chuỗi này ra màn hình:

```php
<?php
echo true; // "1"
echo false; // "" (không hiển thị gì)
```

### Chuyển đổi tự động

```php
<?php
/*
    Trong các phép so sánh và phép tính số học,
    chuỗi được chuyển thành số nếu có thể.
*/
$qty = 20;
if ($qty == '20') {
    echo 'Equal';
} // Equal

$total = 100;
$qty = "20 pieces";
$total = $total + $qty;

echo $total; // 120

/*
    Khi thực hiện phép giữa số nguyên
    và số thực, số nguyên được chuyển
    thành số thực.
*/
$int_number = 100;
$float_number = 100.1;
$total = $int_number + $float_number;

var_dump($total); // float(200.1)
```
