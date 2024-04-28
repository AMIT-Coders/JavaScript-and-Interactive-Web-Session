# AMIT Coders
## Full-Stack web development Bootcamp
### Milestone: 2
#### Session outline:
* Quick wrap-up on the previous session **15 mins**
* Practice jQuery **2 hours**
* Finish Individual work (To-Do App) -- :hourglass_flowing_sand: **2 hours**

:warning: :warning: :warning: :warning: :warning: :warning: :warning:
```diff
- You have to commit and push your code to GitHub at the end of each session.
```
:warning: :warning: :warning: :warning: :warning: :warning: :warning:
***
## To-Do App

To-Do is a task management app to help you stay organized and manage your day-to-day. To-do lists can help you get, and stay, on top of important projects and piles of tasks or decisions. For instance, imagine you're heading a team that's working on a project. There are so many tasks to do, and so many people doing them, that staying on top of it all seems overwhelming.

![To-do-app](https://media.geeksforgeeks.org/wp-content/uploads/20210125180924/20210125180802.gif)

> [!NOTE]  
> As shown above the idea of a To-Do App is to add and remove elements from the webpage.


## How it works 
1. Set up your project.
  a. Create a folder for your project. Inside this folder, create the following files:
```
      index.html  
      styles.css  
      scripts.js
```
2. Write the HTML (index.html).
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple To-Do App</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="todo-container">
        <h1>My To-Do List</h1>
        <input type="text" id="todo-input" placeholder="Add a new task">
        <button id="add-todo">Add Task</button>
        <ul id="todo-list"></ul>
    </div>
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script src="scripts.js"></script>
</body>
</html>
```
3. Style the HTML (styles.css)
```
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
}

.todo-container {
    background: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0,0,0,0.1);
    width: 300px;
}

#todo-list {
    list-style: none;
    padding: 0;
}

#todo-list li {
    padding: 10px;
    border-bottom: 1px solid #ddd;
}

#todo-list li:last-child {
    border-bottom: none;
}

input[type="text"] {
    width: calc(100% - 22px);
    padding: 10px;
    margin-bottom: 10px;
    border: 1px solid #ddd;
    border-radius: 4px;
}

button {
    width: 100%;
    padding: 10px;
    background-color: #5cb85c;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}
```
4. Add functionality with jQuery (scripts.js)

> [!CAUTION] 
> Reference Error  
> Possible Causes: Typos, incorrect variable names, accessing non-existent elements  
> Troubleshooting Steps: Check for typos, verify variable names, ensure element existence, use console.log for debugging, implement error handling techniques

```
$(document).ready(function() {
    $('#add-todo').click(function() {
        var newTask = $('#todo-input').val();
        if (newTask) {
            $('#todo-list').append('<li>' + newTask + '<button class="delete">Delete</button></li>');
            $('#todo-input').val(''); // clear the input after adding
        }
    });

    $('#todo-list').on('click', '.delete', function() {
        $(this).parent().remove();
    });
});

```
> [!IMPORTANT]  
> This JavaScript uses jQuery to handle the addition and removal of tasks. When the "Add Task" button is clicked, it checks if the input is not empty and adds a new item to the list. It also includes a delete button for each task, which, when clicked, removes the task from the list.


 
## Testing and tweaking
* Now you can open your index.html in a browser and see your To-Do app in action.   
* Test it to make sure everything works as expected.  
* You might want to add features like editing tasks or marking them as completed :wink:

***
To effectively test the functionality of the To-Do App created using HTML, CSS, and jQuery, you can create a set of manual test cases. These test cases will help ensure that your app behaves as expected. Here are some test cases you could use:
#### Test Case 1: Adding a New Task
Objective: Verify that the user can add a new task to the to-do list.

Steps:

1. Open the application in a web browser.
2. Locate the input field and enter a task name, e.g., "Buy groceries".
3. Click the "Add Task" button.
Expected Result:  
```
The task "Buy groceries" appears in the list below the input field.
The input field is cleared after the task is added.
```
Actual Result:  
```
To be filled during testing
```
Status: Pass/Fail


***

Update `README.md` todo list below:
- [ ] Add and remove elements successfully.
- [ ] Test manually the functionality.
- [ ] Submit the To-Do App on GitHub.

:white_check_mark: Use `git status` to list all new or modified files that haven't yet been committed.

<p align="center">
  <b>Created by</b><br>
  <b>Mohamed Ibrahim Hany</b>
</p>
