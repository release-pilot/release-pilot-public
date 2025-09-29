## **Monthly Planner 🚀**

<p align="center">
    <img src="./Single_mainlogo_tm.png" alt="Release Planner Icon"  height="100%">
</p>

An interactive calendar-based task planner that lets you add, view, and manage tasks by day, with localStorage persistence and JSON import/export.

### Route
- Path: `/monthly-planner`
- A shortcut card is also available on the `Home` screen.

### Key Features
- Calendar month view with month/year selector
- Add tasks per-day via modal
- Fields: task name, assignee, effort, referenceId, comment, startDate, endDate
- Remove tasks from a given day
- Per-day task indicator dot in the grid when tasks exist
- Animated, modern UI with creative bottom section listing all tasks grouped by date
- Local persistence using `localStorage`
- JSON export and import (validated), with backfill for older imports
- Release Pilot logo branding on the planner header

### How It Works
1. Navigate to `/monthly-planner`.
2. Change month/year using the controls at the top.
3. For any day cell, click "Add" to open the modal and enter task details. Start/End dates default to the selected day.
4. Tasks added for a day appear in the day’s modal table and influence the per-day indicator dot.
5. Scroll down to see "All Tasks by Date". Each date shows task cards with metadata badges and comments.
6. Click Export to download the current task dataset as JSON. Click Import to load a previously exported JSON dataset.

### Data Persistence
- All tasks are saved under the storage key: `monthlyPlanner.tasks.v1`.
- Data is auto-loaded on mount and auto-saved on any change.
- Import automatically normalizes older entries by injecting `startDate` and `endDate` if missing.

### JSON Shape
The exported/imported structure is a dictionary keyed by date (`YYYY-MM-DD`) with arrays of tasks.

```json
{
  "2025-09-29": [
    {
      "id": "1730200000000-abc123",
      "taskName": "Design review",
      "assignee": "Priya",
      "effort": "4h",
      "referenceId": "RP-42",
      "comment": "Focus on accessibility",
      "startDate": "2025-09-29",
      "endDate": "2025-09-29"
    }
  ]
}
```

### UI/UX Details
- Day cells animate in and show a subtle green dot if the day has tasks.
- The tasks-by-date list uses animated cards with colored badges for assignee, effort, reference links, and dates.
- Modal and overlay feature smooth fade/scale animations.
- Release Pilot logo appears beside the "Monthly Planner" title.

### Implementation Notes
- Component: `src/components/monthly-planner/MonthlyPlanner.tsx`
- Styles/animations: `src/components/monthly-planner/MonthlyPlanner.css`
- Home entry: `src/components/Home.tsx` (adds a card linking to `/monthly-planner`)

### Extensibility Ideas
- Show task count badges in day cells (hover tooltip or pill)
- Drag to create multi-day tasks
- Filter and search across bottom task list
- Sync with backend service or team calendar
- Color labels or avatar chips for assignees

### Known Limitations
- No conflict detection between overlapping tasks
- Import replaces current dataset (no merge UI yet)
- No timezone customization (uses browser locale for date handling)


