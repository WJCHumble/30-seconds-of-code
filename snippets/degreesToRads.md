---
方法名: degreesToRads
标签: 数学，初级
---

将角度从度转为弧。

- 使用 `Math.PI` 和度转为弧度的公式来将角度从度转为弧。

```js
const degreesToRads = deg => (deg * Math.PI) / 180.0;
```

```js
degreesToRads(90.0); // ~1.5708
```