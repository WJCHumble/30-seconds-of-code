---
方法名: digitize
标签: 数学，初级
---

将数字转为数字数组，必要时移除它的符号。

- 使用 `Math.abs()` 把数字的符号去掉。
- 将数字转为字符串，使用展开运算符（`...`）来构造数组。
- 使用 `Array.prototype.map()` 和 `parseInt()` 将每个值转为整型。

```js
const digitize = n => [...`${Math.abs(n)}`].map(i => parseInt(i));
```

```js
digitize(123); // [1, 2, 3]
digitize(-123); // [1, 2, 3]
```
