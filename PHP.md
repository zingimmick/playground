# PHP 的一些特殊情况（个人向）

### in_array

[文档](https://www.php.net/manual/en/function.in-array)

检查数组中是否存在某个值

> 在 PHP 8.0.0 之前，string needle 在非严格模式下将会匹配数组中的值 0，反之亦然。这可能会导致不希望的结果。其它类型也存在类似的边缘情况。如果不是绝对确定有关值的类型，请始终使用 strict flag 以避免意外行为。

```php
echo in_array('', [0, 1, 2]) ? 1 : 0; // 0
echo in_array(null, [0, 1, 2]) ? 1 : 0; // 1
echo in_array(false, [0, 1, 2]) ? 1 : 0; // 1
echo in_array(0, ['a', 'b', 'c']) ? 1 : 0; // 1
```

