---
方法名: any
标签: 数组，初级
---

检查所提供的函数是否为数组中至少一个元素返回 `ture`

- 使用 `Array.prototype.some()` 来测试是否数组中有元素基于 `fn` 返回 `true`
- 省略第二个参数 `fn`，会将 `Boolean` 作为默认值。

```js
const any = (arr, fn = Boolean) => arr.some(fn);
```

```js
any([0, 1, 2, 0], x => x >= 2); // true
any([0, 0, 1, 0]); // true
```
