---
方法名: addWeekDays
标签: 日期，中级
---


在添加了给定的工作日后计算日前

- 使用 `Array.from()` 来构造一个数组，该数组的长度等于要添加的工作日的计数。
- 使用 `Array.prototype.reduce()` 来迭代数组，从 `startDate` 开始增加，使用 `Date.prototype.getDate()` 和 `Date.prototype.setDate()`。
- 如果当前的 `date` 是周末，通过添加一天或两天让它变成工作日来再次更新它。
- **注意:** 不考虑法定节假日

```js
const addWeekDays = (startDate, count) =>
  Array.from({ length: count }).reduce(date => {
    date = new Date(date.setDate(date.getDate() + 1));
    if (date.getDay() % 6 === 0)
      date = new Date(date.setDate(date.getDate() + (date.getDay() / 6 + 1)));
    return date;
  }, startDate);
```

```js
addWeekDays(new Date('Oct 09, 2020'), 5); // 'Oct 16, 2020'
addWeekDays(new Date('Oct 12, 2020'), 5); // 'Oct 19, 2020'
```
