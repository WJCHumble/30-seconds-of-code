---
方法名: copySign
标签: 符号，初级
---

返回第一个数字的绝对值，但是返回的是第二个值的符号。

- 使用 `Math.sign()` 来检查是否两个数字有相同的符号。
- 返回 `x` 如果它们一样，否则返回 `-x`。

```js
const copySign = (x, y) => Math.sign(x) === Math.sign(y) ? x : -x;
```

```js
copySign(2, 3); // 2
copySign(2, -3); // -2
copySign(-2, 3); // 2
copySign(-2, -3); // -2
```
