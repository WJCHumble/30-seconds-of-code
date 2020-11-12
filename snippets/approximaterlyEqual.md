---
方法名: approximatelyEqual
标签: 数学，初级
---

检查两个数字是否大致相等。

- 使用 `Math.abs()` 将两个数的绝对值之差和 `epsilon` 比较。
- 省略第三个参数 `epsilon` 时，将会使用 `0.001` 来作为默认值。 

```js
const approximatelyEqual = (v1, v2, epsilon = 0.001) =>
  Math.abs(v1 - v2) < epsilon;
```

```js
approximatelyEqual(Math.PI / 2.0, 1.5708); // true
```
