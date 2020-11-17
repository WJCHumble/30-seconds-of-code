---
方法名: factorial
标签: 数学，递归，初级
---

计算一个数的阶乘。

- 使用递归。
- 如果 `n` 小于或等于 `1`，则返回 `1`。
- 否则，返回 `n` 的乘积和 `n-1` 的阶乘。
- 如果 `n` 是负数的话，则返回 `TypeError`。

```js
const factorial = n =>
  n < 0
    ? (() => {
        throw new TypeError('Negative numbers are not allowed!');
      })()
    : n <= 1
    ? 1
    : n * factorial(n - 1);
```

```js
factorial(6); // 720
```
