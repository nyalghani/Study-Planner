# Study Planner

A Python command-line app for organizing courses, tracking assignment deadlines, and marking work as complete.

## Features

- Add, view, and delete courses and assignments.
- Set or update deadlines and view assignments for a specific course.
- See unfinished assignments due today or later, sorted by deadline.
- Save courses and assignments locally so they’re available the next time you run the app.

## How to run

Requires Python 3.10 or newer. No extra packages are needed.

Open a terminal in the project folder and run:

```bash
python study_tracker.py
```

To try it out, add a course such as `CS 135`, then add an assignment and set its deadline in `DD/MM/YYYY` format. Select **View Upcoming Assignments** to see it in the deadline list.

## How it works

The tracker stores data in `courses.txt` next to the script. It creates the file when you save your first course. Assignments are stored under their course, so two courses can each have an assignment named `Quiz 1`. When saving changes, the app writes to a temporary file before replacing `courses.txt` so an interrupted write doesn’t leave a partially written save.
