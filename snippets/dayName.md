---
方法名: dayName
标签: 日期，初级
---

从 `Date` 对象上获取工作日的名称。

- 使用 `Date.prototype.toLocaleDateString()` 以及 `{ weekday: 'long' }` 选项来检索工作日。
- 使用可选的第二个参数来获取特定语言的名称，或者省略它使用默认的地区设置。

```js
const dayName = (date, locale) =>
  date.toLocaleDateString(locale, { weekday: 'long' });
```

```js
dayName(new Date()); // 'Saturday'
dayName(new Date('09/23/2020'), 'de-DE'); // 'Samstag'
```
