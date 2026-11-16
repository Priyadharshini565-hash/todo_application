# Ex03 To-Do List using JavaScript
## Date: 16/11/2026

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
index.html
```

<!DOCTYPE html>
<html>
<head>
    <title>To-Do List</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="container">
        <h1>My To-Do List</h1>

        <div class="input-box">
            <input type="text" id="taskInput"
                   placeholder="Enter your task">
            <button onclick="addTask()">Add</button>
        </div>

        <ul id="taskList"></ul>
    </div>

    <script src="script.js"></script>
</body>
</html>
```
style.css
```

body {
    font-family: Arial, sans-serif;
    background-color: #f0f4f8;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
}

.container {
    background: white;
    padding: 25px;
    width: 350px;
    border-radius: 10px;
    box-shadow: 0 0 10px gray;
}

h1 {
    text-align: center;
    color: #333;
}

.input-box {
    display: flex;
    gap: 10px;
}

input {
    flex: 1;
    padding: 10px;
    border: 1px solid gray;
    border-radius: 5px;
}

button {
    padding: 10px;
    background: #007bff;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

li {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px;
    margin-top: 10px;
    background: #eee;
    border-radius: 5px;
}

.completed {
    text-decoration: line-through;
    color: gray;
}

.delete {
    background: red;
}
```
script.js
```

function addTask() {
    let input = document.getElementById("taskInput");
    let task = input.value.trim();

    if (task === "") {
        alert("Please enter a task!");
        return;
    }

    let li = document.createElement("li");

    let span = document.createElement("span");
    span.textContent = task;

    span.onclick = function() {
        span.classList.toggle("completed");
    };

    let btn = document.createElement("button");
    btn.textContent = "Delete";
    btn.className = "delete";

    btn.onclick = function() {
        li.remove();
    };

    li.appendChild(span);
    li.appendChild(btn);

    document.getElementById("taskList").appendChild(li);

    input.value = "";
}
```


## OUTPUT
![alt text](<Screenshot 2026-11-16 211855.png>)
## RESULT
The program for creating To-do list using JavaScript is executed successfully.
