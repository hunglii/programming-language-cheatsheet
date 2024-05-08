# Biến

## Khai báo biến

```php
$variable_name = value;
```

## Đặt tên biến

Tên biến phải:
- có tiền tố `$` (dấu đô la);
- kí tự đầu tiên (sau dấu `$`) phải là chữ cái (`a-z`) hoặc dấu gạch dưới `_`;
- các kí tự còn lại có thể là chữ cái, chữ số, dấu gạch dưới `_`.

## Hiển thị giá trị biến

Trong tệp tin chỉ chứa PHP:

```php
<?php
echo $variable_name;
```

Trong tài liệu HTML:

```php
<?php echo $variable_name; ?>
```

hoặc dùng cú pháp rút gọn sau:

```php
<?= $variable_name ?>
```