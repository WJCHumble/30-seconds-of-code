---
方法名: coalesce
标签: 类型，初级
---

返回第一个定义了的不为 null 的参数

- 使用 `Array.prototype.find()` 和 `Array.prototype.includes()` 来发现第一个不等于 `undefined` 或 `null` 的值。

```js
const coalesce = (...args) => args.find(v => ![undefined, null].includes(v));
```

```js
coalesce(null, undefined, '', NaN, 'Waldo'); // ''
```
