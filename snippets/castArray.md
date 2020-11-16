---
方法名: castArray
标签: 类型，数组，初级
---

如果提供的值不是数组，则将它转为数组。

- 使用 `Array.prototype.isArray()` 来确定 `val` 是否为数组，并按原样返回或相应地封装在数组中。

```js
const castArray = val => (Array.isArray(val) ? val : [val]);
```

```js
castArray('foo'); // ['foo']
castArray([1]); // [1]
```
