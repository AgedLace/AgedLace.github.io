---
Title: New Row For Multiple Value Fields
Type: Dataview Query Template
Created: 2023 September 04, 02:23:18 pm
Modified: 2023 September 08, 04:56:23 pm
Tags: Dataview/Templates/New-Row-Multiple-Field-Values
---

**Source** - [Dataview: Create new row for multiple-value field - Help - Obsidian Forum](https://forum.obsidian.md/t/dataview-create-new-row-for-multiple-value-field/66194)

---

## A New Row for Multiple-value Fields

Given notes with the following frontmatter

```
type: idea
status: done
reference: Genesis 19; Genesis 18; Luke 24
```

and the following desired output

```
REFERENCE      |  NOTES
---------------------------
Genesis 19     | Note 3
----------------------------
Matthew 24     | Note 1
                 Note 4
                 Note7
---------------------------
Revelation 2   | Note 5
                 Note 7
```

the dataview query needs to be …

```
TABLE rows.file.link AS "Note"
FROM "my notes"
WHERE reference
FLATTEN reference
SORT reference
```
