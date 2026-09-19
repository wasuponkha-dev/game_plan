---
type: dashboard
updated: 2026-09-19
---

# ⏱️ สถิติเวลาเล่น

## รวมทั้งหมด

```dataview
TABLE WITHOUT ID
  file.link AS "เกม",
  playtime AS "ชม.",
  completion + "%" AS "คืบหน้า",
  round(playtime / completion * 100, 1) AS "ชม. ที่คาดว่าจะใช้ทั้งหมด"
FROM "10-Games"
WHERE file.name = "00-Index" AND playtime > 0
SORT playtime DESC
```

## บันทึกรายเดือน

| เดือน | ชม. รวม | เกมที่จบ | หมายเหตุ |
|---|---|---|---|
| 2026-09 | | | |
