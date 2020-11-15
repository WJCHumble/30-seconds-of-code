---
方法名: createDirIfNotExists
标签: node，初级
---

创建一个目录，如果它不存在。

- 使用 `fs.existsSync()` 来检查目录是否存在，使用 `fs.mkdirSync()` 来创建目录。

```js
const fs = require('fs');

const createDirIfNotExists = dir => (!fs.existsSync(dir) ? fs.mkdirSync(dir) : undefined);
```

```js
createDirIfNotExists('test');
// creates the directory 'test', if it doesn't exist
```
