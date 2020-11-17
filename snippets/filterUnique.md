---
方法名: filterUnique
标签: 数组，初级
---

使用筛选出来的唯一值创建数组。

- 使用 `new Set()` 和 `...` 展开运算符在 `arr` 中创建一个唯一值的数组。
- 使用 `Array.prototype.filter()` 来创建只包含唯一值的数组。

```js
const filterNonUnique = arr =>
  [...new Set(arr)].filter(i => arr.indexOf(i) === arr.lastIndexOf(i));
```

```js
filterNonUnique([1, 2, 2, 3, 4, 4, 5]); // [1, 3, 5]
```
