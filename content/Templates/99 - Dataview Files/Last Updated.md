---
Created: 2023 October 10, 01:35:11 pm
Modified:  2023 October 10, 03:34:43 pm
---

```dataview
TABLE dateformat(file.mtime, "MMM dd yyyy") AS "Last Modified"
FROM ""
SORT file.mtime DESC
LIMIT 25
```
