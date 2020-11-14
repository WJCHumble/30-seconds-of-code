---
方法名: compactWhitespace
标签: string,regexp,beginner
---

压缩字符串中的空白。

- 使用 `String.prototype.replace()` 和正则表达式来将所有出现的 2 个或更多空白字符串替换为单个空格。

```js
const compactWhitespace = str => str.replace(/\s{2,}/g, ' ');
```

```js
compactWhitespace('Lorem    Ipsum'); // 'Lorem Ipsum'
compactWhitespace('Lorem \n Ipsum'); // 'Lorem Ipsum'
```
