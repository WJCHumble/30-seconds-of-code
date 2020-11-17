---
方法名: expandTabs
标签: string,regexp,beginner
---

将 tabs 转为空格，其中每个制表符对应 `count` 空格。

- 使用 `String.prototype.replace()` 、正则表达式、`String.prototype.repeat()` 来将每个 tab 字符替换为 `count` 空格。

```js
const expandTabs = (str, count) => str.replace(/\t/g, ' '.repeat(count));
```

```js
expandTabs('\t\tlorem', 3); // '      lorem'
```
