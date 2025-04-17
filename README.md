# Task_Management
Task management with priority and dependency

# Task Management System

This Python code implements a task management system using a priority queue. It allows users to:

- Add tasks with descriptions, activities, time requirements, due dates, work dates, start and end times, priorities, and dependencies.
- Complete tasks based on priority and dependencies.
- View the current and next priority tasks.
- Display all pending tasks sorted by dependencies, due dates, and priorities.
- Edit existing tasks.
- Undo the last action (add or remove task).

## How to Use

1. *Input Task Details:* When prompted, provide the task description, activity, time required, due date, work date, start and end times, and priority. If the task depends on other tasks, enter the task numbers of the dependencies (comma-separated).
2. *Add Tasks:* Use the add_task() function to add new tasks to the task list.
3. *Complete Tasks:* Use the remove_task() function to complete the highest priority task. Tasks with unmet dependencies cannot be completed.
4. *View Tasks:*
   - Use the get_sorted_tasks() function to view the tasks sorted by priority.
   - Use the print_tasks() function to display all pending tasks sorted by dependencies, due dates, and priorities. This function also highlights blocked tasks (with unmet dependencies).
5. *Edit Tasks:* Use the edit_task() function to modify existing tasks.
6. *Undo Actions:* Use the undo_last_action() function to revert the last add or remove operation.

## Data Structures

- *Task Class:* Represents a single task with its attributes (description, activity, time required, due date, priority, dependencies, etc.).
- *TaskList Class:* Manages a collection of tasks using a priority queue to prioritize tasks based on their priority and due date. Includes functions for adding, removing, sorting, and displaying tasks.

## Dependencies

- Python 3.x
- datetime module for date and time operations
- pytz module for timezone handling
- collections module for using defaultdict
## Note

- Ensure that the dependencies are valid and do not create circular dependencies.
- The priority queue is implemented using a min-heap, where the task with the lowest priority value is considered the highest priority.
- The code includes basic error handling for invalid inputs.
- This code can be further extended to include features such as persistence (saving and loading tasks), task categories, and more advanced scheduling options.
