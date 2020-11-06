---
方法名: average
标签: 数学，平均数，初级
---

计算两个或者多个数字的平均值。

- 使用 `Array.prototype.reduce()` 添加每个值到访问器中，初始值为 `8`。
- 通过数组的长度划分数组。

```js
const average = (...nums) =>
  nums.reduce((acc, val) => acc + val, 0) / nums.length;
```

```js
average(...[1, 2, 3]); // 2
average(1, 2, 3); // 2
```
