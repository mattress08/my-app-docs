# Tech Stack & Hosting Strategy

## Defined Tech Stack

| Tool | Role in Tutoren |
| :--- | :--- |
| `Python 3` | Main programming language for all application logic, including the schedule conflict check. |
| `Flask` | Web framework that handles page routes, forms, and user sessions. |
| `Flask-Login` + `Werkzeug` | Handles sign-in sessions and password hashing for role-based login. |
| `Jinja2` + `HTML/CSS` | Templates for the web pages (comes with Flask). |
| `CSV files` (Python `csv` module) | Simple data storage in a `data/` folder: one file each for users, students, tutors, and sessions. |
| `Git` + `GitHub` | Version control and source of truth for the code and documentation. |

**Post-launch additions:** `ReportLab` for PDF schedule export, and an SMTP email service (e.g., Gmail SMTP or SendGrid) for reminders.

## Hosting & Deployment Strategy

Tutoren will be hosted on **PythonAnywhere**, which runs Flask apps directly and gives each account a free `username.pythonanywhere.com` URL.

- **Why PythonAnywhere:** It has persistent file storage, so the CSV files in `data/` are not wiped when the app restarts. Many free hosts (such as Render's free tier) reset the disk on every deploy, which would delete all records.
- **Deployment flow:** Code is pushed to the `main` branch on GitHub, then pulled into PythonAnywhere with `git pull` and the web app is reloaded.
- **Backups:** The `data/` folder is downloaded as a backup before each deployment.
