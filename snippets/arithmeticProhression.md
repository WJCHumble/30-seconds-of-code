---
方法名: arithmeticProgression
标签: 数学，初级
---

在算术级数中创建一个数字数组，从给定的正整数开始，一直到指定的限制。

- 使用 `Array.from()` 来创建一个所需长度（`lim/n`）的数组，并且使用 `map` 函数来给它填充指定范围内所需要的值。

```js
const arithmeticProgression  = (n, lim) => 
  Array.from({ length: Math.ceil(lim / n) }, (_, i) => (i + 1) * n );
```

```js
arithmeticProgression(5, 25); // [5, 10, 15, 20, 25]
```
