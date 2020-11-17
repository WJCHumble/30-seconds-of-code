---
方法名: either
标签: 函数，逻辑，初级
---

检查对于给定的参数集是否至少有一个函数会返回 `true`。

- 在使用提供的参赛 `args` 调用函数的结果上使用逻辑与运算符（`||`）
- Use the logical or (`||`) operator on the result of calling the two functions with the supplied `args`.

```js
const either = (f, g) => (...args) => f(...args) || g(...args);
```

```js
const isEven = num => num % 2 === 0;
const isPositive = num => num > 0;
const isPositiveOrEven = either(isPositive, isEven);
isPositiveOrEven(4); // true
isPositiveOrEven(3); // true
```
