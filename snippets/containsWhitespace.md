---
方法名: containsWhitespace
标签: 字符串，正则，初级
---

检查是否给定的字符串中有空字符。

- 使用 `RegExp.prototype.test()` 和合适正则表达式来检查是否给定的字符串包含空字符。

```js
const containsWhitespace = str => /\s/.test(str);
```

```js
containsWhitespace('lorem'); // false
containsWhitespace('lorem ipsum'); // true
```
