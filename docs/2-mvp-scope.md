# MVP Scope & Feature Backlog

## The Ultimate Product Vision

Tutoren is a cloud based management app for small tutoring centers. It will lets managers keep track of students, tutors, and employees, assign students to tutors, and build conflict-free schedules without spreadsheets or double bookings.

## The Launch Goal (v1.0 MVP)

To launch a functional version by **December 12, 2026**, focusing strictly on core value: getting people into the system and onto a schedule with no double bookings.

## Feature Prioritization Matrix

### Must Have (MVP Lineup)

| Feature | Description | Why it's critical for launch |
| :--- | :--- | :--- |
| `Role-Based Login` | Managers, Tutors, and Employees sign in with their own accounts and only see what their role allows. | Student and staff records are private. Without access control, the app can't be used safely by anyone. |
| `People Management & Assignment` | Managers add, edit, and delete students, tutors, and employees, and assign students to tutors. | This is the data every other feature depends on. No people, no schedule. |
| `Schedule Management with Conflict Check` | Managers create tutoring sessions; the app blocks any session that overlaps an existing one for the same tutor or student. | Preventing double bookings is the core problem Tutoren solves. |

### Nice to Have (Post-Launch Backlog)

| Feature | Description | Why it can wait |
| :--- | :--- | :--- |
| `PDF Schedule Export` | Export a tutor's or student's schedule as a printable PDF. | Users can view schedules in the browser at launch. PDF is a convenience, not the core value. |
| `Email Reminders` | Automatically email students and tutors before upcoming sessions. | Needs an outside email service and a background job, which adds cost and risk. Reminders only help once scheduling already works. |
