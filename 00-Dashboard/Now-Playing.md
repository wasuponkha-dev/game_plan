---
type: dashboard
updated: 2026-09-19
---

# 🎮 กำลังเล่นอยู่

> [!tip] วิธีใช้
> ตารางนี้คือสถานะรวมทุกเกม — อัปเดตทุกครั้งที่จบ session
> ถ้าติดตั้ง plugin **Dataview** แล้ว ตารางล่างจะอัปเดตเองจาก frontmatter ของ `10-Games/*/00-Index.md`

## สถานะรวม

```dataview
TABLE
  status AS "สถานะ",
  completion + "%" AS "ความคืบหน้า",
  platform AS "เครื่อง",
  playtime AS "ชม.",
  last_played AS "เล่นล่าสุด"
FROM "10-Games"
WHERE file.name = "00-Index" AND status != "backlog"
SORT completion DESC
```

## ตารางสำรอง (เขียนมือ — ใช้ถ้ายังไม่มี Dataview)

| เกม | สถานะ | % | เครื่อง | เล่นล่าสุด | ค้างอยู่ตรงไหน |
|---|---|---|---|---|---|
| [[10-Games/Digimon-World-3/00-Index|Digimon World 3]] | กำลังเล่น | ? | PS1 | 2026-09-20 | Badge 3/4 · Partner ครบ 8/8 ✅ |

## ⚠️ เตือนของพลาดที่ใกล้ถึง

```dataview
TASK
FROM "10-Games"
WHERE contains(file.name, "Missables") AND !completed
LIMIT 20
```

---

## ลิงก์ด่วน

- [[Backlog]] — คิวเกมที่รอเล่น
- [[Completed-100]] — หอเกียรติยศ
- [[Playtime-Log]] — สถิติเวลา
