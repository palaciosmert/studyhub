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