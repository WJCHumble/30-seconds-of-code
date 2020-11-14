---
方法名: clampNumber
标签: 数学，初级
---

在边界值 `a` 和 `b` 指定的包含范围内限制 `num`。

- 如果 `num` 超出了范围，则返回 `num`。
- 否则，返回范围内最近的数字。

```js
const clampNumber = (num, a, b) =>
  Math.max(Math.min(num, Math.max(a, b)), Math.min(a, b));
```

```js
clampNumber(2, 3, 5); // 3
clampNumber(1, -1, -5); // -1
```
