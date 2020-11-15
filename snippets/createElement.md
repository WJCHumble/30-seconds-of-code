---
方法名: createElement
标签: browser，初级
---

根据字符串创建元素（没有添加到文档中的）
如果给定的字符串含有多个元素，只会返回第一个。

- 使用 `Document.createElement()` 来创建一个新的元素。
- 使用 `Element.innerHTML` 将其内部的 HTML 设为提供的字符串参数。
- 使用 `ParentNode.firstElementChild` 来返回字符串的元素版本。

```js
const createElement = str => {
  const el = document.createElement('div');
  el.innerHTML = str;
  return el.firstElementChild;
};
```

```js
const el = createElement(
  `<div class="container">
    <p>Hello!</p>
  </div>`
);
console.log(el.className); // 'container'
```
