---
方法名: addDaysToDate
标签: 时间，中级
---

计算给定日期的天数 `n` 的日期，返回它字符串的表现形式。

- 使用 `new Date` 从第一个参数创建 date 对象。
- 使用 `Date.prototype.getDate()` 和 `Date.prototype.setDate()` 添加 `n` 天到给定的 date。
- 使用 `Date.prototype.toISOString()` 返回一个 `yyyy-mm-dd` 格式的字符串。

```js
const addDaysToDate = (date, n) => {
  d = new Date(date);
  d.setDate(d.getDate() + n);
  return d.toISOString().split('T')[0];
};
```

```js
addDaysToDate('2020-10-15', 10); // '2020-10-25'
addDaysToDate('2020-10-15', -10); // '2020-10-05'
```
