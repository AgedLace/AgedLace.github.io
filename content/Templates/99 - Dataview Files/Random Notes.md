---
Created: 2010 October 23, 02:40:33 pm
Modified:  2023 October 10, 03:34:50 pm
---

```dataviewjs
let docs = dv.pages('#quote');
var randos = (docs) => {return docs.sort(() => .5 - Math.random()).slice(0,5)};

dv.list(randos(docs).map(e => e.file.link));
```
