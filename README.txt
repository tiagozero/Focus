═══════════════════════════════════════════════════════════════════
  FOCUS — Pomodoro Tracker
  README & Feature Guide
═══════════════════════════════════════════════════════════════════

OVERVIEW
────────
FOCUS is a single-file, browser-based productivity tracker built
around the Pomodoro technique. Open index.html in any modern
browser — no installation, no server, no internet required.

All data is saved automatically to your browser's localStorage,
so everything persists across page refreshes and browser restarts.


───────────────────────────────────────────────────────────────────
  GETTING STARTED
───────────────────────────────────────────────────────────────────

1. Open index.html in Chrome, Edge, Firefox, or Safari.
2. Click "+ Add Activity" or press N to create your first task.
3. Click ▶ to start the timer. The progress bar fills as time elapses.
4. When the timer hits zero, the task is marked complete automatically.

That's it. Everything else is optional.


───────────────────────────────────────────────────────────────────
  ACTIVITIES (TASKS)
───────────────────────────────────────────────────────────────────

Each activity row contains:

  • TIMER         — Countdown displayed on the left. Shows remaining
                    time in MM:SS or H:MM:SS format. Turns orange
                    and pulses in the final 60 seconds.

  • PROGRESS BAR  — Fills left-to-right as the timer runs. The
                    percentage is shown on the left side of the bar.

  • TASK NAME     — Click on the bar area and type to name the task.
                    The name is centered and readable at all times.

  • ▶ START       — Starts or pauses the timer.
                    · ▶  = Start / Resume
                    · ⏸  = Pause
                    · ✓  = Done (task complete)

  • PRIORITY PILL — Cycles between HIGH / MED / LOW when clicked.
                    Color-coded: red = high, amber = med, green = low.

  • ⧉ PiP         — Opens Picture-in-Picture mode (see PiP section).

  • ⚙ SETTINGS    — Opens a per-task popup to configure:
                      · Priority (High / Med / Low)
                      · Start Time (time-block scheduling)
                      · Goal Time (duration in minutes)
                      · Tags (type + Enter to add, × to remove)
                      · Reset Timer / Delete task

  • × DELETE      — Removes the task immediately.

  • DRAG HANDLE   — The ⠿ icon on the far left. Click and drag to
                    reorder tasks.

Auto-save: Tasks are saved to localStorage on every change and
every 5 seconds while a timer is running, so the exact remaining
time is preserved even after a page refresh.


───────────────────────────────────────────────────────────────────
  SUB-TASKS
───────────────────────────────────────────────────────────────────

Each activity can have unlimited sub-tasks, useful for breaking
work into smaller steps.

  OPENING SUB-TASKS
  · In Table view:  Click the "▶ SUB-TASKS" header inside the row
                    to expand the list inline.
  · In Timeline view: Sub-tasks are shown directly on each card.
  · From anywhere:  Click ＋ next to the sub-tasks header to open
                    the Sub-Task popup modal.

  ADDING SUB-TASKS
  · Type a name in the "New sub-task name…" field.
  · Set the duration in minutes.
  · Press Enter or click ＋ Add.

  EACH SUB-TASK HAS:
  · ○ / ✓  — Toggle done state.
  · Name    — Editable inline.
  · Timer   — Countdown for this sub-task specifically.
  · ▶ / ⏸  — Start or pause the sub-task timer. Starting a
               sub-task also starts the parent task timer.
  · −1m / +1m — Adjust time in 1-minute increments.
  · Tags    — Type a tag + Enter/comma to add. Click × to remove.
               Tags are shown as colored chips below each sub-task.
  · ×       — Delete the sub-task.

  When sub-tasks are added, the parent task's goal time is
  automatically updated to the sum of all sub-task durations.


───────────────────────────────────────────────────────────────────
  VIEWS
───────────────────────────────────────────────────────────────────

Switch between views inside ⚙ Settings → View.

  TABLE VIEW (default)
  · Classic spreadsheet-style list.
  · Tasks are shown as rows with the timer on the left, the
    progress bar in the center, and action buttons overlaid
    on the right side of the bar.
  · A vertical line separates the timer from the task area.
  · Sub-tasks expand inline below the task bar.

  TIMELINE VIEW
  · Tasks are laid out as nodes on a winding snake path,
    3 per row, alternating direction (left→right, right→left).
  · Each card shows: name, live countdown, progress bar,
    priority pill, percentage, inline sub-task list, and
    action buttons.
  · Sub-tasks are visible directly on the card with their
    own timers, start buttons, delete buttons, and tag rows.
  · The ▶ toggle in the Sub-tasks header collapses/expands
    the sub-task list on each card.
  · ＋ in the sub-tasks header opens the full popup modal
    to add new sub-tasks.


───────────────────────────────────────────────────────────────────
  PICTURE IN PICTURE (PiP)
───────────────────────────────────────────────────────────────────

Click the ⧉ button on any task to launch a PiP timer.

  NATIVE PiP (Chrome/Edge on HTTPS)
  · A real OS-level floating window appears above ALL other
    apps and browser tabs.
  · Shows: task name, live countdown, progress bar, status.
  · Stays visible even when you switch to another tab,
    application, or fullscreen video.
  · Closes automatically when the task finishes.

  FALLBACK PiP (all browsers)
  · If native PiP is unavailable (HTTP, Firefox, older Safari),
    a draggable floating panel appears over the page instead.
  · Drag it by the header to reposition anywhere on screen.
  · Shows task name, timer, progress bar, ▶/⏸ button, and ⚙.
  · Click ⧉ again or ✕ to close.


───────────────────────────────────────────────────────────────────
  FOCUS MODE
───────────────────────────────────────────────────────────────────

Click ⊙ Focus in the header (or press F) to enter Focus Lock.

· Fills the entire screen with the current running task.
· Shows the task name, a giant countdown timer, progress bar,
  and any sub-tasks with their own timers.
· ⏸ / ▶ pause and resume.
· ✕ or Esc exits Focus mode.

Use Focus mode when you want zero distractions.


───────────────────────────────────────────────────────────────────
  STATS BAR
───────────────────────────────────────────────────────────────────

Four live counters at the top of the page:

  · Sessions   — Number of tasks completed today.
  · Min Focused — Total minutes of focused work logged.
  · Tasks Done  — Total tasks marked complete.
  · Min Planned — Total minutes currently planned across all tasks.

Stats are saved persistently. Use Reset Stats (in ⚙ Settings →
Data) to clear them for a new day.


───────────────────────────────────────────────────────────────────
  DAILY ACHIEVEMENTS
───────────────────────────────────────────────────────────────────

Hidden by default. Toggle in ⚙ Settings → Achievements →
"Show Achievements".

A row of 9 milestone chips that unlock as you work:

  ✅  First Task    — Complete your first task
  ⏱️  1 Hour        — Focus for 60 minutes total
  🔥  3 Sessions    — Complete 3 sessions
  ⚡  5 Sessions    — Complete 5 sessions
  💪  3 Hours       — Focus for 3 hours total
  🧠  6 Hours       — Focus for 6 hours total
  🚀  8 Hours       — Focus for 8 hours total
  🏆  10 Hours      — Focus for 10 hours total
  🌟  8 Sessions    — Complete 8 sessions

A toast notification pops up when you unlock a new achievement.
Chips turn orange and show a ✓ badge when unlocked.


───────────────────────────────────────────────────────────────────
  SESSION HISTORY
───────────────────────────────────────────────────────────────────

A collapsible panel below the tasks shows every completed session.

Each entry shows:
  · Task name
  · Tags associated with the task
  · Time of completion
  · Duration in minutes

Click the header to collapse/expand. Click "Clear" to wipe history.


───────────────────────────────────────────────────────────────────
  GOALS (Tools → Goals)
───────────────────────────────────────────────────────────────────

Track cumulative time toward named targets.

  CREATING A GOAL
  · Give it a name (e.g. "Deep Work").
  · Set a tag to track (e.g. "work") — any task tagged with this
    will count toward the goal.
  · Set a target in minutes (e.g. 300 for 5 hours).

  HOW IT WORKS
  · Every time you complete a task that has a matching tag, the
    minutes are added to the goal's progress.
  · The goal card shows a progress bar, percentage complete, and
    session count.
  · Goals persist across days and accumulate over time.


───────────────────────────────────────────────────────────────────
  TEMPLATES (Tools → Templates)
───────────────────────────────────────────────────────────────────

Save your current task list as a reusable template.

  SAVING
  · Type a template name in the box and click Save Template.
  · The current set of tasks (names, durations, priorities,
    tags, sub-tasks) is saved.

  LOADING
  · Click the template name to expand and preview its tasks.
  · Click Load to apply:
      · Replace — clears current tasks and loads the template.
      · Append  — adds template tasks to the existing list.

  Useful for recurring daily routines or project setups.


───────────────────────────────────────────────────────────────────
  SAVED DAYS (Tools → Saved Days)
───────────────────────────────────────────────────────────────────

Save a snapshot of the entire day when you finish.

  HOW TO SAVE
  · Click 🏁 Finish Day in the header.
  · Review your summary (total time, activities, completion rate).
  · Click ✓ Save Day to archive it.

  WHAT'S SAVED
  · Day name, date, total focus time, completion percentage,
    and the full list of activities with durations and tags.

  VIEWING SAVED DAYS
  · Open Tools → Saved Days to see all archived days.
  · Each entry shows stats, a completion bar, and activity tags.


───────────────────────────────────────────────────────────────────
  TIME BLOCKING
───────────────────────────────────────────────────────────────────

Assign a scheduled start time to any task.

· Open ⚙ task settings → Start Time (Time Block).
· Set a time (e.g. 09:30).
· The time appears as a small pill inside the task bar (⏰ 09:30).
· Use this to plan your day in time slots.


───────────────────────────────────────────────────────────────────
  THEMES & CUSTOMIZATION
───────────────────────────────────────────────────────────────────

Open ⚙ Settings to customize the look.

  THEMES (5 built-in)
  · Brutalist — High-contrast black/white with orange accents.
  · Midnight  — Dark purple, inspired by developer night mode.
  · Paper     — Off-white, serif fonts, quiet and minimal.
  · Forest    — Deep green, earthy and calm.
  · Neon      — Black with cyan/magenta glows.

  PROGRESS BAR COLOR
  · Choose from 8 presets or pick a custom color.
  · Applies to all task progress bars immediately.

  VIEW
  · Switch between Table and Timeline views.

  KEYBOARD SHORTCUTS
  · /    — Focus the search bar.
  · N    — Add a new activity.
  · G    — Open Goals panel.
  · T    — Open Templates panel.
  · S    — Open Saved Days panel.
  · Esc  — Close any open panel/modal.


───────────────────────────────────────────────────────────────────
  DATA & BACKUP
───────────────────────────────────────────────────────────────────

All data is stored in your browser's localStorage under these keys:

  pomo_rows        — Current task list (names, timers, sub-tasks)
  pomo_stats       — Sessions, minutes, tasks counters
  pomo_history     — Completed session log
  pomo_goals       — Goals list and progress
  pomo_saved_days  — Archived finished days
  pomo_templates   — Saved templates
  pomo_theme       — Active theme
  pomo_prog_color  — Progress bar color
  pomo_day_name    — Current day label
  pomo_ach_visible — Whether achievements bar is shown
  pomo_view        — Last active view (table or timeline)

  EXPORT / IMPORT
  · Open Tools → Data tab.
  · Export Backup — downloads a JSON file with all your data.
  · Import Backup — restores data from a previously exported file.
  · Export CSV    — exports session history as a spreadsheet.

  RESET
  · Reset Stats   — clears sessions/minutes/tasks counters only.
  · Clear All Data — wipes everything and reloads fresh.

  NOTE: localStorage is browser-specific. Data does not sync
  between browsers or devices. Use Export Backup to transfer data.


───────────────────────────────────────────────────────────────────
  SEARCH
───────────────────────────────────────────────────────────────────

· Click the search bar or press / to search activities.
· Filters tasks in real-time by name or tag.
· Non-matching tasks are hidden; matching ones remain visible.
· Press Esc or click ✕ to clear the search.


───────────────────────────────────────────────────────────────────
  DAY PROGRESS BAR
───────────────────────────────────────────────────────────────────

A thin bar below the stats shows how much of today's planned
work has been completed. Calculated as:
  (minutes completed) / (total minutes planned) × 100%


───────────────────────────────────────────────────────────────────
  TECHNICAL NOTES
───────────────────────────────────────────────────────────────────

· Single HTML file — no build step, no dependencies, no server.
· Works offline after first open.
· Native PiP requires Chrome or Edge on HTTPS (or localhost).
· Tested on Chrome 120+, Edge 120+, Firefox 122+, Safari 17+.
· Timer precision: ±1 second (JavaScript setInterval).
· Auto-saves every 5 seconds while a timer is running.


───────────────────────────────────────────────────────────────────
  CREDITS
───────────────────────────────────────────────────────────────────

FOCUS — Pomodoro Tracker
Built as a single-file web application.
No frameworks. No dependencies. Pure HTML, CSS, and JavaScript.

═══════════════════════════════════════════════════════════════════
