# TODO App Specification

## Overview

A simple TODO application built with vanilla HTML/CSS/JavaScript in a single file.
This project is part of the ACP test (OpenClaw -> GitHub -> Claude Code).

Related: [GitHub Issue #1](https://github.com/scs-yasu/todo-test/issues/1)

## Functional Requirements

1. **Add Task** - User can add a new task by entering text and submitting
2. **Toggle Complete** - User can toggle a task between completed and incomplete states
3. **Delete Task** - User can delete a task from the list
4. **Persistent Storage** - All tasks are saved to localStorage and restored on page load

## Tech Stack

- HTML5
- CSS3
- Vanilla JavaScript (no frameworks or libraries)

## File Structure

```
todo-test/
├── index.html    # Single-file app (HTML + CSS + JS)
├── SPEC.md       # This specification
└── README.md     # Project overview (if needed)
```

## UI Description

### Layout

- Centered container with a clean, minimal design
- Header with the app title "TODO App"
- Input area at the top for adding new tasks
- Task list below the input area

### Components

#### Input Area
- Text input field with placeholder text (e.g., "Add a new task...")
- "Add" button to submit the task
- Enter key also submits the task

#### Task List
- Each task displays:
  - A checkbox or clickable area to toggle completion
  - The task text (with strikethrough style when completed)
  - A delete button (e.g., "x" or trash icon)
- Completed tasks are visually distinguished (e.g., strikethrough text, muted color)
- Empty state message when no tasks exist

### Interactions
- Adding a task with empty text is prevented
- Newly added tasks appear at the top or bottom of the list
- Toggling completion updates both the UI and localStorage
- Deleting a task removes it from both the UI and localStorage

## Data Model

Tasks are stored in localStorage as a JSON array:

```json
[
  {
    "id": 1,
    "text": "Buy groceries",
    "completed": false
  }
]
```

- `id` (number) - Unique identifier (timestamp-based)
- `text` (string) - Task description
- `completed` (boolean) - Completion status
