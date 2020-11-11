---
方法名: both
标签: 函数，逻辑，初学者
---

检查两个给定的函数是否为给定参赛都返回 `true`。

- 对提供的 `args` 调用两个函数的结果，并使用逻辑与（`&&`）运算符

```js
const both = (f, g) => (...args) => f(...args) && g(...args);
```

```js
const isEven = num => num % 2 === 0;
const isPositive = num => num > 0;
const isPositiveEven = both(isEven, isPositive);
isPositiveEven(4); // true
isPositiveEven(-2); // false
```
