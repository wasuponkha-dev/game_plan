---
type: dashboard
updated: 2026-09-19
---

# 🏆 หอเกียรติยศ — จบ 100% แล้ว

```dataview
TABLE
  platform AS "เครื่อง",
  playtime AS "ชม. ที่ใช้",
  completed_date AS "วันที่จบ",
  rating AS "คะแนน"
FROM "10-Games"
WHERE file.name = "00-Index" AND status = "100%"
SORT completed_date DESC
```

## ตารางสำรอง

| เกม | เครื่อง | ชม. | วันที่จบ | คะแนน | บทเรียนที่ได้ |
|---|---|---|---|---|---|
| _(ยังไม่มี)_ | | | | | |
