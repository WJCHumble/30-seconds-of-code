---
方法名: daysAgo
标签: 日期，时间
---

以字符串表现形式计算从今天开始 `n` 天前的日前。

- 使用 `new Date` 来获取当前的日前，`Math.abs()` 和 `Date.prototype.getDate()` 相应地更新日前，并且使用 `Date.prototype.setDate()` 设置结果。
- 使用 `Date.prototype.toISOString()` 来会返回 `yyyy-mm-dd` 格式的字符串。

```js
const daysAgo = n => {
  let d = new Date();
  d.setDate(d.getDate() - Math.abs(n));
  return d.toISOString().split('T')[0];
};
```

```js
daysAgo(20); // 2020-09-16 (if current date is 2020-10-06)
```
