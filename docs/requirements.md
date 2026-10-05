# StudyHub – Requirements

## 1. User Stories

### Account

#### US-01: Create an account
**As a** student, **I want to** create an account, **so that** my courses and tasks are private to me.

**Acceptance criteria:**
- The registration form asks for a username, email and password.
- A user cannot register with an email that is already in use.
- After registering, the user is redirected to the login page.

#### US-02: Log in
**As a** student, **I want to** log in with my email and password, **so that** I can access my own courses and tasks.

**Acceptance criteria:**
- An error message is shown if the email or password is incorrect.
- After logging in, the user is redirected to the dashboard.
- Pages that require an account cannot be opened without logging in.

#### US-03: Log out
**As a** student, **I want to** log out, **so that** nobody else can see my data on a shared computer.

**Acceptance criteria:**
- A "Log out" link is visible on every page while logged in.
- After logging out, the user is redirected to the login page.

### Courses

#### US-04: Add a course
**As a** student, **I want to** add the courses I am taking this semester, **so that** I can organize my tasks by course.

**Acceptance criteria:**
- The course form asks for a course name.
- An error message is shown if the course name is empty.
- The new course appears in the course list.

#### US-05: View my courses
**As a** student, **I want to** see a list of all my courses, **so that** I can quickly open the one I need.

**Acceptance criteria:**
- The course list shows only the courses of the logged-in user.
- Each course shows how many unfinished tasks it has.
- A message such as "You have no courses yet" is shown if the list is empty.

#### US-06: Edit a course
**As a** student, **I want to** rename a course, **so that** I can fix mistakes I made while adding it.

**Acceptance criteria:**
- The edit form is pre-filled with the current course name.
- An error message is shown if the new name is empty.

#### US-07: Delete a course
**As a** student, **I want to** delete a course, **so that** my course list only shows the courses I am currently taking.

**Acceptance criteria:**
- Each course has a clearly visible delete button.
- The user is asked for confirmation before the course is deleted.
- After deletion, the course no longer appears in the list.
- All tasks that belong to the deleted course are also deleted.

### Tasks

#### US-08: Add a task to a course
**As a** student, **I want to** add an assignment, project or exam to a course, **so that** all my work for that course is in one place.

**Acceptance criteria:**
- The task form asks for a title, a type (assignment, project or exam) and a due date.
- An error message is shown if the title is empty.
- The new task appears on the course's page.

#### US-09: Set a due date for a task
**As a** student, **I want to** set a due date for a task, **so that** I don't miss the deadline.

**Acceptance criteria:**
- The task form has a date field.
- An error message is shown if the date field is left empty.
- The saved date is displayed in the task list.

#### US-10: Update the status of a task
**As a** student, **I want to** mark a task as "To do", "In progress" or "Done", **so that** I can track my progress.

**Acceptance criteria:**
- Every new task starts with the status "To do".
- The user can change the status from the task list.
- Tasks marked as "Done" are visually different (e.g. greyed out).

#### US-11: Edit a task
**As a** student, **I want to** edit a task, **so that** I can update it when a deadline is changed.

**Acceptance criteria:**
- The edit form is pre-filled with the current task details.
- The same validation rules as in US-08 and US-09 apply.

#### US-12: Delete a task
**As a** student, **I want to** delete a task, **so that** tasks added by mistake don't clutter my list.

**Acceptance criteria:**
- The user is asked for confirmation before the task is deleted.
- After deletion, the task no longer appears in any list.

### Dashboard

#### US-13: See upcoming deadlines
**As a** student, **I want to** see my upcoming deadlines from all courses on one page when I log in, **so that** I immediately know what I need to work on next.

**Acceptance criteria:**
- The dashboard lists unfinished tasks from all courses, sorted by due date (closest first).
- Each task shows its title, course name, type and due date.
- Tasks marked as "Done" are not shown on the dashboard.

#### US-14: Notice overdue tasks
**As a** student, **I want to** clearly see tasks whose due date has passed, **so that** I can deal with them as soon as possible.

**Acceptance criteria:**
- Unfinished tasks with a past due date are highlighted (e.g. in red).
- Overdue tasks are listed at the top of the dashboard.


## 2. Functional Requirements

| ID | Requirement | Related Story |
|----|-------------|---------------|
| FR-01 | The system shall allow a user to register with a username, email and password. | US-01 |
| FR-02 | The system shall reject registration if the email is already in use. | US-01 |
| FR-03 | The system shall allow a registered user to log in with their email and password. | US-02 |
| FR-04 | The system shall display an error message when login credentials are incorrect. | US-02 |
| FR-05 | The system shall redirect users who are not logged in to the login page when they try to open a protected page. | US-02 |
| FR-06 | The system shall allow a logged-in user to log out. | US-03 |
| FR-07 | The system shall allow a user to create a course by entering a course name. | US-04 |
| FR-08 | The system shall display a list of the user's courses with the number of unfinished tasks in each course. | US-05 |
| FR-09 | The system shall allow a user to rename a course. | US-06 |
| FR-10 | The system shall ask for confirmation before deleting a course or a task. | US-07, US-12 |
| FR-11 | The system shall delete all tasks of a course when the course is deleted. | US-07 |
| FR-12 | The system shall allow a user to create a task with a title, type (assignment, project or exam) and due date. | US-08, US-09 |
| FR-13 | The system shall reject a task if its title or due date is empty. | US-08, US-09 |
| FR-14 | The system shall assign the status "To do" to every new task. | US-10 |
| FR-15 | The system shall allow a user to change a task's status to "To do", "In progress" or "Done". | US-10 |
| FR-16 | The system shall allow a user to edit and delete a task. | US-11, US-12 |
| FR-17 | The system shall display all unfinished tasks from all courses on the dashboard, sorted by due date. | US-13 |
| FR-18 | The system shall highlight unfinished tasks whose due date has passed and list them at the top of the dashboard. | US-14 |

## 3. Non-Functional Requirements

| ID | Category | Requirement |
|----|----------|-------------|
| NFR-01 | Security | User passwords shall be stored as hashes, never as plain text. |
| NFR-02 | Security | A user shall only be able to view, edit or delete their own courses and tasks. |
| NFR-03 | Security | Secret keys and configuration values shall not be stored in the Git repository. |
| NFR-04 | Usability | Every form shall display a clear error message next to the invalid field. |
| NFR-05 | Usability | A new user shall be able to register and add their first course within 2 minutes without help. |
| NFR-06 | Compatibility | The application shall work on the latest versions of Chrome, Firefox and Safari. |
| NFR-07 | Compatibility | All pages shall be usable on screens 375px wide or wider (mobile phones). |
| NFR-08 | Performance | Every page shall load in under 2 seconds on a local machine. |
| NFR-09 | Maintainability | The README shall include step-by-step instructions to install and run the project. |
| NFR-10 | Maintainability | The code shall follow the PEP 8 style guide. |



## 4. MVP Scope (MoSCoW)

| Story | Title | Priority |
|-------|-------|----------|
| US-01 | Create an account | Must |
| US-02 | Log in | Must |
| US-03 | Log out | Must |
| US-04 | Add a course | Must |
| US-05 | View my courses | Must |
| US-06 | Edit a course | Could |
| US-07 | Delete a course | Should |
| US-08 | Add a task to a course | Must |
| US-09 | Set a due date for a task | Must |
| US-10 | Update the status of a task | Must |
| US-11 | Edit a task | Should |
| US-12 | Delete a task | Should |
| US-13 | See upcoming deadlines | Must |
| US-14 | Notice overdue tasks | Should |