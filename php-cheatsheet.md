# PHP Cheatsheet

## Cú pháp

### Xác định khối mã PHP

**Cách xác định khối mã PHP trong tài liệu HTML**

```php
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="utf-8">
    <title>Chèn PHP vào HTML</title>
</head>
<body>
    <h1><?php echo 'PHP trong HTML'; ?></h1>
</body>
</html>
```

**Cách xác định khối mã PHP trong tập tin**

Có thể bỏ qua thẻ đóng PHP: `?>`

```php
<?php
echo 'PHP trong tệp';
```

### Phân biệt chữ hoa, chữ thường

PHP phân biệt chữ hoa, chữ thường đối với:
- Các cấu trúc như `if`, `if-else`, `if-elseif`, `switch`, `while`, `do-while`...
- Các từ khóa như `true` và `false`.
- Tên các hàm do người dùng định nghĩa và tên các lớp.

### Câu lệnh

Một chương trình (kịch bản) PHP bao gồm một hoặc nhiều câu lệnh. Một câu lệnh là một đoạn mã thực hiện một công việc gì đó.

Một câu lệnh đơn luôn kết thúc với một dấu chấm phảy (`;`):

```php
$message = "Hello";
```

Tuy nhiên, câu lệnh đơn đứng ngay trước thẻ đóng PHP `?>` thì không cần kết thúc bằng dấu chấm phảy:

```php
<?php echo $name ?>
```

Một câu lệnh phúc tạp bao gồm một hoặc nhiều câu lệnh đơn đặt trong cặp dấu ngoặc `{` và `}`. Bạn không cần đặt dấu chấm phảy sau `}`:

```php
if ($is_new_user) {
    send_welcome_email();
}
```

### Khoảng trắng và xuống dòng

Trong hầu hết trường hợp, các khoảng trắng (tạo ra khi bấm phím cách hoặc Tab) và xuống dòng (tạo ra khi bấm phím Enter) bị trình biên dịch bỏ qua. Do đó bạn có thể thêm các khoảng trắng hoặc xuống dòng để đoạn mã trông đẹp mắt và dễ đọc hơn.

```php
login(
    $username,
    $password
);
```

