---
方法名: accumulate
标签: 数学，数组，中级
---

创建一个部分和的数组。

- 使用 `Array.prototype.reduce()` 来对 `nums` 进行累加。
- 使用 `Array.prototype.slice(-1)` 、展开运算符（`...`）和 `+` 运算符加到包含先前总和的累加器数组中。

```js
const accumulate = (...nums) =>
  nums.reduce((acc, n) => [...acc, n + +acc.slice(-1)], []);
```

```js
accumulate(1, 2, 3, 4); // [1, 3, 6, 10]
accumulate(...[1, 2, 3, 4]); // [1, 3, 6, 10]
```
