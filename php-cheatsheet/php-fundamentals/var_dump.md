# var_dump

Xuất ra thông tin của biến, ví dụ: kiểu biến, giá trị biến...

```php
<?php
$balance = 100;
$message = 'Insufficient balance';

var_dump($balance); // int(100)
var_dump($message); // string(20) "Insufficient balance"
```