# FocusFlow – Productivity Intelligence Platform

A professional, framework-free productivity dashboard built with **HTML5, CSS3, Vanilla JavaScript ES6+, Chart.js, and LocalStorage**.

## Features

- Dashboard with task KPIs, productivity score, focus time and streaks
- Full task CRUD
- Priorities: Low, Medium, High, Critical
- Due dates, categories, estimates, search, filters and sorting
- Drag-and-drop manual task ordering
- Pomodoro-style Focus Mode
- Custom focus duration from 5–120 minutes
- Short and long breaks
- Automatic focus-session tracking
- Habit creation, daily check-ins, weekly calendar and streak tracking
- Productivity scoring based on completion, focus, streak, overdue load and habit consistency
- Analytics charts:
  - Tasks completed per day
  - Focus time per day
  - Productivity score
  - Priority distribution
  - Weekly completion rate
- In-app notifications for overdue/upcoming tasks and completed work
- Light/dark/system appearance
- Responsive mobile navigation
- Toast notifications
- Modal forms
- Loading state, empty states and completion confetti
- JSON export/import
- Demo data loader
- All application data persists locally in the browser

## Files

```text
focusflow/
├── index.html
├── style.css
├── script.js
└── README.md
```

## Run

No build step is required.

1. Put all four files in the same folder.
2. Open `index.html` in a modern browser.
3. Internet access is only needed for the Chart.js CDN and Google Fonts; the productivity data itself is stored locally.

For best results, serve the folder with a simple local server, for example:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Data storage

FocusFlow stores application state under the LocalStorage key:

`focusflow_v1`

Nothing is sent to a backend.

Use **Settings → Data & privacy → Export data** to create a JSON backup, and **Import JSON** to restore one.

## Productivity score

The score is a transparent 0–100 calculation:

- Task completion: up to 35 points
- Focus goal progress: up to 25 points
- Focus streak: up to 15 points
- Overdue-task health: up to 15 points
- Habit consistency: up to 10 points

The score is intentionally simple and inspectable so it can be customized without a backend.

## Browser support

Designed for current Chrome, Edge, Firefox and Safari releases with support for ES6+, LocalStorage, drag-and-drop, Canvas and modern CSS.

## Notes

- Browser notifications are implemented as in-app notification cards rather than requiring OS notification permissions.
- Focus sessions are recorded when a focus timer reaches zero.
- Closing or refreshing the page while a timer is running does not persist an unfinished timer.
- The application contains no framework or build dependency.
