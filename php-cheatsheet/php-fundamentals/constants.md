##Hằng

## Định nghĩa hằng

```php
<?php
define( 'WIDTH', '1140px' );
echo WIDTH;
```

Có thể định nghĩa một hằng bất cứ lúc nào trong khi chạy chương trình:

```php
<?php
if (condition) {
    define( 'WIDTH', '1140px' );
}
```

Tên hằng được định nghĩa có thể lấy từ một biến, hằng hoặc biểu thức khác:

```php
$constant_name = 'WIDTH';
define( $constant_name, '1140px' );
```

## Khai báo hằng

```php
const CONSTANT_NAME = value;
```

Các hằng được tạo ra bởi `const` có ngay khi chương trình được biên dịch.