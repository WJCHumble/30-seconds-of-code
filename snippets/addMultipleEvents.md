---
方法名: addMultipleListeners
标签: 浏览器，事件，中级
---

将具有相同的事件处理程序的不同事件添加到一个元素上。

- 使用 `Array.protoype.forEach()` 和 `EventTarget.addEventListener()` 添加多个分配了回掉的事件监听器到一个元素上。

```js
const addMultipleListeners = (el, types, listener, options, useCapture) => {
  types.forEach(type =>
    el.addEventListener(type, listener, options, useCapture)
  );
};
```

```js
addMultipleListeners(
  document.querySelector('.my-element'),
  ['click', 'mousedown'],
  () => { console.log('hello!') }
);
```
