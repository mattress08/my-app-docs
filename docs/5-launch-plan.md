# Go-To-Market & Launch Checklist

## Marketing & User Acquisition

* **Primary Launch Channel:** Direct outreach to small tutoring centers and campus tutoring services. We will start with a free pilot for one or two local tutoring centers and offer setup help in person, then grow through their referrals. Our first 50 users are the managers, tutors, and staff at those pilot centers.
* **Value Proposition:** *"Tutoren schedules your students and tutors in one place and never lets you double-book a session."*

## Pre-Launch Deployment Checklist

- [ ] Verify all code changes are merged into the `main` production branch
- [ ] Test every role (Manager, Tutor, Employee) and confirm each one only sees the pages it is allowed to
- [ ] Test form submissions with bad input (empty fields, invalid dates, duplicate names) and confirm clear error messages
- [ ] Try to create overlapping sessions for the same tutor and the same student, and confirm the app blocks both
- [ ] Run a cross-browser usability check (Chrome, Safari, Mobile screens)
- [ ] Back up the `data/` folder

## Launch Day Operations

- [ ] Pull the latest `main` branch on PythonAnywhere, reload the web app, and check the live production URL
- [ ] Conduct live verification testing directly on the hosted platform: log in as each role and book one test session
- [ ] Create the pilot center's Manager account and walk them through adding their first tutors and students
- [ ] Send the announcement email to pilot centers and post it on our marketing channels
- [ ] Watch the PythonAnywhere error log during the first day and fix any blocking bugs
