---
方法名: arrayToCSV
标签: 数组，字符串，中级
---

将一个 2 维数组转化为一个用逗号分割的字符串。

- 使用 `Array.prototype.map()` 和 `Array.prototype.join(delimiter)` 将 1 维数组合并为一个字符串。
- 使用 `Array.prototype.join('\n')` 将所有 1 维数组合并为一个字符串，并用换行符分割开每个 1 维数组。
- 省略第二个参数 `delimiter` 时，会使用 `,` 来作为默认值。

```js
const arrayToCSV = (arr, delimiter = ',') =>
  arr
    .map(v =>
      v.map(x => (isNaN(x) ? `"${x.replace(/"/g, '""')}"` : x)).join(delimiter)
    )
    .join('\n');
```

```js
arrayToCSV([['a', 'b'], ['c', 'd']]); // '"a","b"\n"c","d"'
arrayToCSV([['a', 'b'], ['c', 'd']], ';'); // '"a";"b"\n"c";"d"'
arrayToCSV([['a', '"b" great'], ['c', 3.1415]]);
// '"a","""b"" great"\n"c",3.1415'
```

