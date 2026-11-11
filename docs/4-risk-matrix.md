# Risk Mitigation & Technical Constraints

## Core Technical Risks

* **Highest Risk Feature:** Schedule Management with Conflict Check
* **The Hazard:**
  * **Overlap logic is easy to get wrong.** Sessions can partly overlap, sit back-to-back, or repeat weekly. One missed case lets a double booking through, which breaks the app's main promise.
  * **CSV files don't handle simultaneous writes.** If two managers save a session at the same moment, one save can overwrite the other or corrupt the file.
  * **Time zones and date formats.** Mixing formats (e.g., `11/12` vs `12/11`) can place sessions on the wrong day.

## The Pivot Strategy

If our primary implementation for this feature fails or takes too long, our backup plan is to:

1. **Simplify the scheduling model.** Drop free-form start and end times and use fixed one-hour time slots (e.g., Mon 16:00, Mon 17:00). A conflict then becomes a simple check: "is this tutor or student already booked in this slot?" Recurring weekly sessions are pushed to the backlog.
2. **Limit who can write.** Only the Manager role can create or edit sessions, so there is just one writer at a time. Every save writes to a temporary file first and then replaces the real CSV, so a crash never leaves a half-written file.
3. **Switch storage if CSV still breaks.** Move session data to SQLite, which ships with Python and supports safe simultaneous writes, while keeping the rest of the CSV files unchanged.
