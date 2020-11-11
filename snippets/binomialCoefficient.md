---
方法名: binomialCoefficient
标签: 数学，初学者
---


Calculates the number of ways to choose `k` items from `n` items without repetition and without order.

- 使用 `Number.isNaN()` 来检查两个值中是否存在 `isNaN`。
- 检查 `k` 是否小于 `0`，大于或等于 `n`，等于 `1` 或 `n-1`，并返回合适的结果。
- 检查 `n-k` 是否小于 `k`，并相应的交换它们的值。
- 从 `2` 到 `k` 循环，并计算二项式系数。
- 使用 `Math.round()` 来考虑计算中的舍入误差。

```js
const binomialCoefficient = (n, k) => {
  if (Number.isNaN(n) || Number.isNaN(k)) return NaN;
  if (k < 0 || k > n) return 0;
  if (k === 0 || k === n) return 1;
  if (k === 1 || k === n - 1) return n;
  if (n - k < k) k = n - k;
  let res = n;
  for (let j = 2; j <= k; j++) res *= (n - j + 1) / j;
  return Math.round(res);
};
```

```js
binomialCoefficient(8, 2); // 28
```
