---
Created: 2023 October 10, 02:29:45 pm
Modified:  2023 October 10, 02:36:52 pm
---

```dataview
TABLE dateformat(file.ctime, "MMM dd yyyy") AS "Date Created"
FROM ""
WHERE file.ctime AND file.ctime <= date(today) - dur(1 month) AND file.ctime >= date(today) - dur(1 month 7 days)
SORT file.ctime DESC
Limit 25
```
