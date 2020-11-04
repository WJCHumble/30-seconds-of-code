---
方法名: allUniqueBy
标签: 数组，中级
---

根据提供的映射函数，检查是否数组中的所有元素都不相等。

- 使用 `Array.prototype.map()` 为 `arr` 的所有元素应用 `fn`。
- 创建一个 `Set` 集合用于保存唯一值。
- 使用 `Array.prototype.length` 和 `Set.prototype.size` 来比较唯一值和原始数组的长度。

```js
const allUniqueBy = (arr, fn) => arr.length === new Set(arr.map(fn)).size;
```

```js
allUniqueBy([1.2, 2.4, 2.9], Math.round); // true
allUniqueBy([1.2, 2.3, 2.4], Math.round); // false
```
