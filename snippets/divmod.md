---
方法名: divmod
标签: 数学，初级
---

- 返回给定数字的商和余数构成的数组。

- 使用 `Math.floor()` 来获取 `x / y` 的商。
- 使用模运算符来获取 `x / y` 的余数。

```js
const divmod = (x, y) => [Math.floor(x / y), x % y];
```

```js
divmod(8, 3); // [2, 2]
divmod(3, 8); // [0, 3]
divmod(5, 5); // [1, 0]
```
