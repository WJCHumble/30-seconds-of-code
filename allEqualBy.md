---
方法名: allEqualBy
标签: 数组,中等
---

根据提供的映射函数，检查是否数组中所有的元素都相等

- 把 `fn` 作为 `arr` 的第一个元素
- 使用 `Array.prototype.every()` 来检查是否 `fn` 对数组中的所有元素返回与第一个元素相同的值。
- 使用严格的比较运算符来比较数组中的元素，这不会考虑 NaN 的自不相等。
  
```js
const allEqualBy = (arr, fn) => {
  const eql = fn(arr[0]);
  return arr.every(val => fn(val) === eql);
};
```

```js
allEqualBy([1.1, 1.2, 1.3], Math.round); // true
allEqualBy([1.1, 1.3, 1.6], Math.round); // false
```
