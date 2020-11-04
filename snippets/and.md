---
title: and
tags: 数学，逻辑，初级
---

检测是否两个参数都为 `true`

- 在两个给定的值上面使用逻辑且 `&&` 运算符

```js
const and = (a, b) => a && b;
```

```js
and(true, true); // true
and(true, false); // false
and(false, false); // false
```
