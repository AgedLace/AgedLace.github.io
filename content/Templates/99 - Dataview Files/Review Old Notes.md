---
Created: 2023 October 10, 02:22:44 pm
Modified:  2023 October 10, 02:40:33 pm
---

```dataview
TABLE dateformat(file.mtime, "MMM dd yyyy") AS "Last Modified"
FROM ""
WHERE file.mtime AND file.mtime <= date(today) - dur(1 month) AND file.mtime >= date(today) - dur(1 month 7 days)
SORT file.mtime DESC
LIMIT 25
```
