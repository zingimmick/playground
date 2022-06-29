# Laravel

## 任务可能在事务提交之前执行

```php
// 👎 Bad 任务可能在事务提交之前执行
$something = DB::transaction(function () {
    // change something
    dispatch(new SomethingChanged($something)); 
});
// 👍 Good 在事务执行完成后分发任务
$something = DB::transaction(function () {
    // change something
});
dispatch(new SomethingChanged($something));
```
