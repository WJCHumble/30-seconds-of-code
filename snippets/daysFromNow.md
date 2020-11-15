---
方法名: daysFromNow
标签: 日期，初级
---

以字符串表现形式计算从今天算起 `n` 天后的日期。

- 使用 `new Date()` 获取当前的日前，`Math.abs()` 和 `Date.prototype.getDate()` 来相应地更新人气，并且使用 `Date.prototype.setDate()` 来设置结果。
- 使用 `Date.prototype.toISOString()` 来返回 `yyyy-mm-dd` 的格式字符串。

```js
const daysFromNow = n => {
  let d = new Date();
  d.setDate(d.getDate() + Math.abs(n));
  return d.toISOString().split('T')[0];
};
```

```js
daysFromNow(5); // 2020-10-13 (if current date is 2020-10-08)
```
