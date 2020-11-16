---
方法名: distance
标签: 数学，初级
---

计算两个点之间的距离。

- 使用 `Math.hypot()` 来计算两个点之间的欧几里德距离。

```js
const distance = (x0, y0, x1, y1) => Math.hypot(x1 - x0, y1 - y0);
```

```js
distance(1, 1, 2, 3); // ~2.2361
```
