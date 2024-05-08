# Kiểu chuỗi

## Tạo chuỗi

```php
<?php
# tạo chuỗi bằng dấu nháy đơn
$title = 'PHP string is awesome';

# tạo chuỗi bằng dấu nháy kép
$title = "PHP string is awesome";
```

## Chèn kí tự đặc biệt vào chuỗi

Cả chuỗi tạo bởi dấu nháy đơn và dấu nháy kép đều có thể chèn các kí tự đặc biệt bằng cách chèn chuỗi thoát tương ứng của chúng:

```php
<?php
$str = 'This is a \'simple\' string';
$str2 = "This is a 'simple' string";
echo $str; // This is a 'simple' string
echo $str2; // This is a 'simple' string

$str = 'The command C:\\*.* will delete all files.';
$str2 = "The command C:\\*.* will delete all files.";
echo $str; // The command C:\*.* will delete all files.
echo $str2; // The command C:\*.* will delete all files.
```

Một số chuỗi thoát của các kí tự đặc biệt:

- `\t` -> tab ngang
- `\\` -> dấu `\`
- `\$` -> kí hiệu đô la $
- `\"` -> dấu nháy kép
- `\'` -> dấu nháy đơn.

## Nội suy chuỗi

Chỉ dùng được với chuỗi tạo bởi cặp dấu nháy kép.

```php
<?php
$name = 'John';
echo "Hello $name"; // Hello John
```

hoặc viết tường minh hơn:

```php
<?php
$name = 'John';
echo "Hello {$name}"; // Hello John
```

## Nối chuỗi

```php
<?php
$name = 'John';
echo 'Hello ' . $name; // Hello John
```

## Truy cập các kí tự trong một chuỗi

Cú pháp:

```php
$str[index]
```

Ví dụ:

```php
<?php
$title = 'PHP string is awesome';

echo $title[0]; // P
```

## Lấy chiều dài của chuỗi

```php
<?php
$title = 'PHP string is awesome';
echo strlen($title); // 21
```

## Heredoc và nowdoc

### Heredoc

Cú pháp:

```php
<?php
$str = <<<IDENTIFIER
đặt một chuỗi ở đây
nó có thể có nhiều dòng
bao gồm dấu nháy đơn và dấu nháy kép
    có thể có khoảng trắng
và cho phép nội suy biến.
IDENTIFIER;
```

Ví dụ:

```php
<?php
$title = 'My site';

$header = <<<HEADER
<header>
    <h1>$title</h1>
</header>
HEADER;

echo $header;
```

### Nowdoc

Tương tự heredoc nhưng không hỗ trợ nội suy biến và `IDENTIFIER` phải được đặt trong dấu nháy đơn:

```php
<?php
$header = <<<'HEADER'
<header>
    <h1>My site</h1>
</header>
HEADER;

echo $header;
```
