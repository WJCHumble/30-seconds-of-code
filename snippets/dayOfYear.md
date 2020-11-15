---
方法名: dayOfYear
标签: 日期，初级
---

从 `Date` 对象上获取一年中的某一天（数值在 1-366 之间）。

- 使用 `new Date()` 和 `Date.prototype.getFullYear()` 来获取一年中的第一天来作为 `Date` 对象。
- 用 `date` 减去一年中的第一天，并且每天的毫秒数得到结果。
- 使用 `Math.floor()` 将得到的数字适当地四舍五入为整数。

```js
const dayOfYear = date =>
  Math.floor((date - new Date(date.getFullYear(), 0, 0)) / 1000 / 60 / 60 / 24);
```

```js
dayOfYear(new Date()); // 272
```
