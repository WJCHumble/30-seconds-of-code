---
方法名: everyNth
标签: 数组，初级
---

返回数组中每个元素的 `nth`。

- 使用 `Array.prototype.filter()` 来创建一个包含给定数组的每个 `nth` 元素的新数组。

```js
const everyNth = (arr, nth) => arr.filter((e, i) => i % nth === nth - 1);
```

```js
everyNth([1, 2, 3, 4, 5, 6], 2); // [ 2, 4, 6 ]
```
