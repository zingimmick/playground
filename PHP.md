# PHP 的一些特殊情况（个人向）

### in_array

[文档](https://www.php.net/manual/en/function.in-array)

检查数组中是否存在某个值

> 如果没有设置 `strict` 为 `true`，会有一些违背习惯的情况

```php
echo in_array('', [0, 1, 2]) ? 1 : 0; // 0
echo in_array(null, [0, 1, 2]) ? 1 : 0; // 1
echo in_array(false, [0, 1, 2]) ? 1 : 0; // 1
```

