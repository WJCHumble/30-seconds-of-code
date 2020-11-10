---
方法名: aperture
标签: 数组，中级
---

创建连续元素的 `n` 元组数组。

- 使用 `Array.prototype.slice()` 和 `Array.prototype.map()` 来创建一个合适长度的数组
- 用 `arr` 中连续元素的 `n` 元组来填充数组。
- 如果 `n` 大于 `arr` 的长度，会返回一个空的数组。

```js
const aperture = (n, arr) =>
  n > arr.length
    ? []
    : arr.slice(n - 1).map((v, i) => arr.slice(i, i + n));
```

```js
aperture(2, [1, 2, 3, 4]); // [[1, 2], [2, 3], [3, 4]]
aperture(3, [1, 2, 3, 4]); // [[1, 2, 3], [2, 3, 4]]
aperture(5, [1, 2, 3, 4]); // []
```
