# PHP Cheatsheet

## Cú pháp

### Thẻ bắt đầu/kết thúc mã PHP

```php
<?php
    // các lệnh PHP ở đây
?>
```

### Câu lệnh

Các câu lệnh được kết thúc bởi dấu chấm phảy.

### Phân biệt chữ hoa, chữ thường

Đối với các từ khóa, tên các hàm, các lớp do người dùng tạo, PHP không phân biệt chữ hoa, chữ thường.

Đối với tên biến, PHP có phân biệt chữ hoa, chữ thường.

### Chú thích

**Chú thích một dòng**

```php
<?php
    # chú thích một dòng bắt đầu bằng dấu #
    // chú thích một dòng cũng có thể bắt đầu bằng //
    echo 'Chào thế giới';
?>
```

**Chú thích nhiều dòng**

```php
<?php
    /* Đây là một ví dụ về chú thích nhiều dòng,
    một chương trình cộng hai số.
    Biến $x là số đầu tiên, biến $y là số thứ hai
    */

    $x = 10;
    $y = 20;
    print "Tổng = " . $x + $y;
?>
```
