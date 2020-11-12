---
方法名: atob
标签: node，字符串，初级
---

解码用 base-64 编码的字符串数据

- 根据给定的 base-64 编码的字符串创建一个 `Buffer`，并且使用 `Buffer.toString('binary')` 来返回解码后的字符串。

```js
const atob = str => Buffer.from(str, 'base64').toString('binary');
```

```js
atob('Zm9vYmFy'); // 'foobar'
```
