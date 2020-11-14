---
方法名: compact
标签: 数组，初级
---

移除数组中的假值。

- 使用 `Array.prototype.filter()` 来过滤假值（`false`、`null`、`0`、`""`、`undefined` 和 `NaN`）。

```js
const compact = arr => arr.filter(Boolean);
```

```js
compact([0, 1, false, 2, '', 3, 'a', 'e' * 23, NaN, 's', 34]); 
// [ 1, 2, 3, 'a', 's', 34 ]
```
