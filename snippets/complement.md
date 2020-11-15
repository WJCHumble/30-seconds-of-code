---
方法名: complement
标签: 函数，逻辑，初级
---

返回一个函数，该函数是给定函数 `fn` 的逻辑补码。

- 在提供 `args` 参数调用 `fn` 的结果使用逻辑运算符 `!` 。

```js
const complement = fn => (...args) => !fn(...args);
```

```js
const isEven = num => num % 2 === 0;
const isOdd = complement(isEven);
isOdd(2); // false
isOdd(3); // true
```
