# Alex User Guide
![Product Website image](docs/Ui.png)


Alex is a smart, friendly, and intuitive task management chatbot. It helps you   keep track of tasks, deadlines, and events effortlessly through a user-friendly interface. With Alex, you can manage your to-dos, schedule important events, and set deadlines. Whether you're looking to organize your day or track long-term projects, Alex has got you covered.

The features Alex provides include:
* Adding Tasks (Deadlines, ToDos, Events, Fixed Duration, Default)
* Marking and Unmarking Tasks
* Deleting Tasks
* Viewing Task List
* Finding Tasks
* Telling User a Joke

## Installation
To download the latest version of Alex,
1. Go to the project's [releases](https://github.com/yikyak02/ip/releases).
2. Download the ```.jar``` file.
3. Run the ```jar``` file by clicking on it.

## Features
## Adding deadlines

Action: Adds a task with a deadline to the task list.

Usage: deadline DESCRIPTION /by DATE

DESCRIPTION: Specify the name of the task (e.g., "Submit report").
DATE: Enter the deadline using the format yyyy-MM-dd HH:mm (e.g., 2024-09-19 15:55) or a valid day of week (e.g Sunday).

**Example Command:**

```
deadline return book /by 2024-09-09 15:55  
```

**Expected Output:**
```
Got it. I've added the following task:
[D][ ] submit project (by: Sep 09 2024 15:55)
Now you have X tasks in the list.
```


## Adding ToDos

Action: Adds a simple to-do task to the task list.

Usage: todo DESCRIPTION

DESCRIPTION: Provide the task description (e.g., "Buy groceries").

**Example Command:**
```
todo buy groceries  
```

**Expected Output:**
```
Got it. I've added the following task:
[T][ ] buy groceries
Now you have X tasks in the list.
```


## Adding Events

Action: Adds an event to the task list, specifying the start and end times.

Usage: event DESCRIPTION /from START /to END

DESCRIPTION: The event name (e.g., "Team meeting").

START: Start day and/or time of the event

END: End day and/or time the event

**Example Command:**
```
event project meeting /from Mon 2pm /to 4pm
````

**Expected Output:**
```
Got it. I've added the following task:
[E][ ] project meeting (from: Mon 2pm to: 4pm)
Now you have X tasks in the list.
```

## Adding Fixed Duration Tasks
Action: Adds a fixed duration task to the task list, specifying the period which the task is active for.

Usage: fixed duration DESCRIPTION (DURATION)

DESCRIPTION: Task name (e.g buy food)

DURATION: Period which task is active for, using the format [X minutes]

**Example Command:**
```
fixed duration buy food (5 minutes)
```

**Expected output:**
```
Got it. I've added the following task:
[F][] buy food (Duration: 5 minutes)
Now you have X tasks in the list.
```

## Adding Default Tasks
Action: Adds a basic task without any additional properties like deadlines or events. Repeats what the user keys in.

Usage: DESCRIPTION

DESCRIPTION: Default task name

**Example Command:**
```
Read book
```

**Expected Output:**
```
Got it. I've added the following task:
added: Read book
Now you have X tasks in the list.
```

## Marking Tasks as Done
Action: Marks a task as done.

Usage: mark TASK_NUMBER

TASK_NUMBER: The number of the task in the list.

**Example Command:**
```
mark 2
```

**Expected Output:**
````
Nice! I've marked this task as done:
[T][X] buy groceries
````

## Unmarking Tasks as not Done
Action: Unmarks a task which was previously done.

Usage: unmark TASK_NUMBER

TASK_NUMBER: The number of the task in the list.

**Example Command:**
```
unmark 2
```

**Expected Output:**
```
OK, I've marked this task as not done yet:
[ ] return book
```
## Deleting Tasks
Action: Deletes a task from the list.

Usage: delete TASK_NUMBER

TASK_NUMBER: The number of the task in the list.

**Example Command:**
```
delete 2
```
**Expected Output:**
```
Deleted task:
[T][X] buy groceries
Now you have X tasks in the list.
```

## Viewing Tasks
Action: Displays all tasks in a numbered list.

Usage: list

**Example Command:**
```
list
```
**Expected Output:**
```
Here are the matching tasks in your list:
1. [T][] buy books
2. [D][] finish work (by Sunday)
3. [T][] pick up gift
```

## Finding Tasks
Action: Find all tasks containing specified keyword

Usage: find TASK_DESCRIPTION

TASK_DESCRIPTION: The description of any task user wants to find from task list.

**Example Command:**
```
find lunch
```
**Expected Output:**
```
Here are the matching tasks in your list:
1. [T][] cook lunch
```

## Telling User a Joke
Action: Tells user a joke for entertainment

Usage: tell me a joke

**Example Command:**
```
tell me a joke
```
**Expected Output:**
```
Why do programmers prefer dark mode? Because the light attracts bugs!
```
## Exiting the chatbot
Action: Cease the program

Usage: bye

**Example Command:**
```
bye
```
**Expected Output:**
```
Bye. Hope to see you again soon!
```
The chatbot window should close 1 second later.

