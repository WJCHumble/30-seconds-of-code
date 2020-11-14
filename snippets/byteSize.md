---
方法名: byteSize
标签: 字符串，初级
---

以字节为单位返回一个字符串。

- 将给定的字符串转化为 [Blob 对象](https://developer.mozilla.org/en-US/docs/Web/API/Blob)。
- 以字节为单位使用 `Blob.size` 来获取字符串的长度。

```js
const byteSize = str => new Blob([str]).size;
```

```js
byteSize('😀'); // 4
byteSize('Hello World'); // 11
```
