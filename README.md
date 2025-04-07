# Ex03 To-Do List using JavaScript
## Date:06/04/2025

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Todo Application</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: pink; 
            text-align: center;
        }
        header, footer {
            background-color: lightblue; 
            color: white;
            padding: 15px;
            font-size: 20px;
            font-weight: bold;
          
        }
        .todo-container {
            max-width: 400px;
            background: white;
            margin: 30px auto;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            border: 2px solid #6da6df;
        }
        .todo-input {
            width: 100%;
            padding: 10px;
            border: 2px solid #6da6df;
            border-radius: 4px;
            margin-bottom: 10px;
        }
        .todo-list {
            list-style: none;
            padding: 0;
        }
        .todo-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px;
            margin-bottom: 5px;
            background-color: #6da6df;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        .todo-item.completed span {
            text-decoration: line-through;
            color: rgb(122, 20, 121);
        }
        .todo-buttons button {
            padding: 5px 10px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        .complete-btn {
            background-color: #6da6df; 
            color: white;
        }
        .delete-btn {
            background-color: #6da6df;
            color: pink;
        }
    </style>
</head>
<body>
```
```
    <header>Todo Application</header>
    <div class="todo-container">
        <h2>To-Do List ✅</h2>
        <input type="text" id="todo-input" class="todo-input" placeholder="Add a new task">
        <ul id="todo-list" class="todo-list"></ul>
    </div>
    <footer>&copy; 2025 Vaishnavi S.A (212223220119) | All rights reserved.</footer>
    <script>
        const todoInput = document.getElementById('todo-input');
        const todoList = document.getElementById('todo-list');

        function addTodo() {
            const task = todoInput.value.trim();
            if (task === '') return;

            const li = document.createElement('li');
            li.className = 'todo-item';

            const span = document.createElement('span');
            span.textContent = task;

            const buttonsDiv = document.createElement('div');
            buttonsDiv.className = 'todo-buttons';

            const completeBtn = document.createElement('button');
            completeBtn.textContent = 'Complete';
            completeBtn.className = 'complete-btn';
            completeBtn.onclick = () => {
                li.classList.toggle('completed');
            };

            const deleteBtn = document.createElement('button');
            deleteBtn.textContent = 'Delete';
            deleteBtn.className = 'delete-btn';
            deleteBtn.onclick = () => {
                todoList.removeChild(li);
            };

            buttonsDiv.appendChild(completeBtn);
            buttonsDiv.appendChild(deleteBtn);

            li.appendChild(span);
            li.appendChild(buttonsDiv);

            todoList.appendChild(li);
            todoInput.value = '';
        }

        todoInput.addEventListener('keypress', (e) => {
            if (e.key === 'Enter') {
                addTodo();
            }
        });
    </script>
</body>
</html>
```

## OUTPUT

![Screenshot 2025-04-07 150030](https://github.com/user-attachments/assets/1e15d08b-7d35-4478-b148-e3087f5dd4fb)




## RESULT
The program for creating To-do list using JavaScript is executed successfully.
