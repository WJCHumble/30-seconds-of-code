---
方法名: allEqual
标签: 数组，初级
---

检查数组中的所有元素是否相等。

- 使用 `Array.prototype.every()` 来检查数组中的所有元素是否都和第一个元素一样。
- 使用严格的比较运算符来比较数组中的元素，这不会考虑 `NaN` 的自不相等。

```js
const allEqual = arr => arr.every(val => val === arr[0]);
```

```js
allEqual([1, 2, 3, 4, 5, 6]); // false
allEqual([1, 1, 1, 1]); // true
```
