---
方法名: all
标签: 数组，初级
---

检查提供的函数是否对数组中的所有值都返回 `true`

- 使用 `Array.prototype.every()`  来测试数组的所有元素是否都在 `fn` 中都返回 `true`
- 省略第二个参数 `fn`，使用 `Boolean` 来作为默认值

```js
const all = (arr, fn = Boolean) => arr.every(fn);
```

```js
all([4, 2, 3], x => x > 1); // true
all([1, 2, 3]); // true
```
