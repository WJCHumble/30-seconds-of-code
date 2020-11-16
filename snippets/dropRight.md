---
方法名: dropRight
标签: 数组，初级
---

创建一个移除了右边起`n` 个元素的数组。

- 使用 `Array.prototype.slice()` 来移除从右边算起制定数字个的元素。
- 省略最后一个参数 `n`，默认值为 `1`。

```js
const dropRight = (arr, n = 1) => arr.slice(0, -n);
```

```js
dropRight([1, 2, 3]); // [1, 2]
dropRight([1, 2, 3], 2); // [1]
dropRight([1, 2, 3], 42); // []
```
