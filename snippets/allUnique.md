---
方法名: allUnique
标签: 数组，初级
---

检查是否数组中的所有元素都不相等。

- 创建一个 `Set` 集合，用于保存唯一值。
- 使用 `Array.prototype.length` 和 `Set.prototype.size` 来比较唯一值和原始数组的长度。

```js
const allUnique = arr => arr.length === new Set(arr).size;
```

```js
allUnique([1, 2, 3, 4]); // true
allUnique([1, 1, 2, 3]); // false
```
