---
aliases:
  - Calendar
  - Timeline
---

# 📅 Calendar Dashboard

> Your timeline — daily notes, meetings, and time-based reflections.
> This is where you **make it whole** by connecting thinking across time.

[[Home Base]] ← Back to Home

---

```button
name 📅 New Daily Note
type command
action QuickAdd: New Daily Note
color green
```
```button
name 🤝 New Meeting Note
type command
action QuickAdd: New Meeting Note
color green
```

---

## 📅 Monthly Calendar

> Click any highlighted day to open its daily note. Navigate months with the arrows.

```dataviewjs
const container = dv.container;
let viewDate = moment();

function renderCalendar(date) {
    container.empty();

    const year = date.year();
    const month = date.month();
    const today = moment();

    // Index existing daily notes by their date string
    const noteMap = {};
    for (const p of dv.pages('"Calendar/Daily Notes"')) {
        const m = p.file.name.match(/(\d{4}-\d{2}-\d{2})/);
        if (m) noteMap[m[1]] = p.file.path;
    }

    // Scoped styles
    const style = container.createEl("style");
    style.textContent = `
        .cal-nav { display:flex; justify-content:space-between; align-items:center; margin-bottom:10px; }
        .cal-nav button {
            cursor:pointer; padding:4px 12px; border-radius:6px;
            border:1px solid var(--background-modifier-border);
            background:var(--background-secondary); color:var(--text-normal);
        }
        .cal-nav button:hover { background:var(--background-modifier-hover); }
        .cal-title { font-size:1.25em; font-weight:700; }
        .cal-today-btn { font-size:0.8em; padding:2px 8px !important; }
        .cal-table { width:100%; border-collapse:collapse; text-align:center; table-layout:fixed; }
        .cal-table th {
            padding:8px 4px; font-size:0.8em; color:var(--text-muted);
            border-bottom:2px solid var(--background-modifier-border);
        }
        .cal-table td { padding:4px; height:40px; vertical-align:middle; }
        .cal-day {
            display:inline-flex; align-items:center; justify-content:center;
            width:34px; height:34px; border-radius:50%; font-size:0.9em;
        }
        .cal-day.has-note {
            background:rgba(148,103,189,0.15); font-weight:600; cursor:pointer;
        }
        .cal-day.has-note:hover { background:rgba(148,103,189,0.35); }
        .cal-day.is-today {
            background:rgba(148,103,189,0.6); color:#fff; font-weight:700;
        }
        .cal-day.is-today.has-note:hover { background:rgba(148,103,189,0.8); }
        .cal-day.no-note { color:var(--text-faint); }
    `;

    // --- Navigation bar ---
    const nav = container.createEl("div", { cls: "cal-nav" });
    const prevBtn = nav.createEl("button", { text: "◀ Prev" });

    const centre = nav.createEl("div", {
        attr: { style: "display:flex;align-items:center;gap:8px;" }
    });
    centre.createEl("span", { text: date.format("MMMM YYYY"), cls: "cal-title" });
    const todayBtn = centre.createEl("button", { text: "Today", cls: "cal-today-btn" });

    const nextBtn = nav.createEl("button", { text: "Next ▶" });

    prevBtn.addEventListener("click", () => {
        viewDate = viewDate.clone().subtract(1, "month");
        renderCalendar(viewDate);
    });
    nextBtn.addEventListener("click", () => {
        viewDate = viewDate.clone().add(1, "month");
        renderCalendar(viewDate);
    });
    todayBtn.addEventListener("click", () => {
        viewDate = moment();
        renderCalendar(viewDate);
    });

    // --- Calendar grid ---
    const table = container.createEl("table", { cls: "cal-table" });
    const thead = table.createEl("thead").createEl("tr");
    for (const d of ["Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat"]) {
        thead.createEl("th", { text: d });
    }

    const tbody = table.createEl("tbody");
    const firstDow = moment([year, month, 1]).day();
    const totalDays = moment([year, month, 1]).daysInMonth();

    let day = 1;
    let row = tbody.createEl("tr");

    // Leading empty cells
    for (let i = 0; i < firstDow; i++) row.createEl("td");

    // Day cells
    for (let col = firstDow; day <= totalDays; col++) {
        if (col > 0 && col % 7 === 0) row = tbody.createEl("tr");

        const cell = row.createEl("td");
        const ds = moment([year, month, day]).format("YYYY-MM-DD");
        const isToday = today.format("YYYY-MM-DD") === ds;
        const notePath = noteMap[ds];

        let cls = "cal-day";
        cls += notePath ? " has-note" : " no-note";
        if (isToday) cls += " is-today";

        const circle = cell.createEl("div", { text: String(day), cls: cls });

        if (notePath) {
            circle.addEventListener("click", () => {
                app.workspace.openLinkText(notePath, "");
            });
        }
        day++;
    }

    // Trailing empty cells
    while (row.children.length < 7) row.createEl("td");
}

renderCalendar(viewDate);
```

---

## 📝 Recent Daily Notes

```dataview
TABLE file.cday AS "Date"
FROM "Calendar/Daily Notes"
SORT file.name DESC
LIMIT 14
```

---

## 🤝 Recent Meetings

```dataview
TABLE date AS "Date", attendees AS "Attendees"
FROM "Calendar/Meetings"
SORT date DESC
LIMIT 10
```

---

## 📆 Daily Notes by Month

> Browse your daily notes grouped by month.

```dataview
TABLE length(rows) AS "# Notes"
FROM "Calendar/Daily Notes"
GROUP BY dateformat(file.cday, "yyyy-MM") AS "Month"
SORT rows[0].file.cday DESC
```

---

## 🕰️ On This Day — Across All Years

> Notes created on today's date in previous years.

```dataview
LIST
FROM ""
WHERE file.cday.month = date(today).month
  AND file.cday.day = date(today).day
  AND file.cday.year != date(today).year
SORT file.cday ASC
```

---

> [!tip] Quick Actions
> - **Create today's daily note:** `Cmd+D` / `Ctrl+D` (or use Daily Notes plugin)
> - **Template:** Use `Templates/Daily Note Template` for consistent structure
> - **Meeting note:** Create a new note in `Calendar/Meetings/` using the Meeting Note Template
