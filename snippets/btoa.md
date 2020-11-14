---
方法名: btoa
标签名: node，字符串，初级
---

从字符串对象创建一个 base 64 编码的 ASCII 字符串，其中字符串中的每个字符都被视为二进制数据中的一个字节。

- 使用二进制编码为给定的字符串创建一个 `Buffer`，并且使用 `Buffer.toString('base')` 来返回编码后的字符串。

```js
const btoa = str => Buffer.from(str, 'binary').toString('base64');
```

```js
btoa('foobar'); // 'Zm9vYmFy'
```
