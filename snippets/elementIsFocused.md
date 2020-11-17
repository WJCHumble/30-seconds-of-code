---
方法名: elementIsFocused
标签: 浏览器，初级
---

检查是否给定的元素是聚焦的。

- 使用 `Document.activeElement` 来决定是否给定的元素是聚焦的。

```js
const elementIsFocused = el => (el === document.activeElement);
```

```js
elementIsFocused(el); // true if the element is focused
```
