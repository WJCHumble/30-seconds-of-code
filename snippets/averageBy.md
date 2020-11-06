---
方法名: averageBy
标签: 数学，数组，中级
---

使用提供的函数将每个元素映射（mapping）到一个值后，计算数组的平均数。

- 使用 `Array.prototype.map()` 将每一个元素映射（map）为 `fn` 返回的值。
- 使用 `Array.prototype.reduce()` 将每个值添加到累加器，初始值为 `0`。
- 根据数组的长度划分数组。

```js
const averageBy = (arr, fn) =>
  arr
    .map(typeof fn === 'function' ? fn : val => val[fn])
    .reduce((acc, val) => acc + val, 0) / arr.length;
```

```js
averageBy([{ n: 4 }, { n: 2 }, { n: 8 }, { n: 6 }], o => o.n); // 5
averageBy([{ n: 4 }, { n: 2 }, { n: 8 }, { n: 6 }], 'n'); // 5
```
