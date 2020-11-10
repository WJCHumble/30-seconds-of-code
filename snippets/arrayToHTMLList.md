---
方法名: arrayToHTMLList
标签: 浏览器，数组，中级
---

将给定的数组元素转为 `<li>` 标签，并且添加到给定的 id 的列表中。

- 使用 `Array.prototype.map()` 和 `Document.querySelector()` 创建一个 html 列表标签

```js
const arrayToHTMLList = (arr, listID) => 
  document.querySelector(`#${listID}`).innerHTML += arr
    .map(item => `<li>${item}</li>`)
    .join('');
```

```js
arrayToHTMLList(['item 1', 'item 2'], 'myListID');
```
