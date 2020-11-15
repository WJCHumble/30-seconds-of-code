---
title: difference
tags: array,beginner
---

计算两个数组的差异，而不过滤重复的值。

- 根据 `b` 创建 `Set` 集合来获取 `b` 中的唯一值。
- 对 `a` 使用 `Array.prototype.filter()` 来保留不在 `b` 中的值，以及使用 `Set.prototype.has()`。

```js
const difference = (a, b) => {
  const s = new Set(b);
  return a.filter(x => !s.has(x));
};
```

```js
difference([1, 2, 3, 3], [1, 2, 4]); // [3, 3]
```
