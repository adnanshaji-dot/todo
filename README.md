# Tickboard

A Kanban-style calendar for Google Tasks, with Google Calendar events.

- Week, Board, Month and Lists views, with one column per task list
- Tap the circle once to start a task (it turns green), tap again to complete it, with a completion sound
- Sections in each list: High priority, Today, Upcoming, No due date, Past
- Drag and drop to reorder, reschedule or move tasks between lists
- Two-way sync with Google Tasks about every 12 seconds, and it works on phones

## Run locally

Double-click `Start Tickboard.bat`, or run `node server.js`, then open http://localhost:5500.

## Google setup

In Google Cloud Console, enable the **Google Tasks API** and **Google Calendar API**. Then create an OAuth client of type *Web application* and add these under **Authorized JavaScript origins**:

- `http://localhost:5500`
- `https://adnanshaji-dot.github.io`

In the OAuth consent screen, add your account under **Audience → Test users**.

"In progress" and "High priority" are saved as `[in progress]` / `[starred]` tags at the end of each task's notes, because the Google Tasks API has no fields for them.
