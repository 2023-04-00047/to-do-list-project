# to-do-list-project
// this is an html project about the things someone wants to do in his or her life
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>To-Do List</title>
</head>
<body>
  <h1>To-Do List</h1>
  <ul id="todo-list"></ul>
  <input type="text" id="new-todo" placeholder="Add a new task">
  <button id="add-button">Add</button>
  <script>
    const todoList = document.getElementById('todo-list');
    const newTodoInput = document.getElementById('new-todo');
    const addButton = document.getElementById('add-button');

    addButton.addEventListener('click', function() {
      const newTodoText = newTodoInput.value;
      if (newTodoText) {
        // Create a new list item for the task
        const newTodoItem = document.createElement('li');
        newTodoItem.innerText = newTodoText;
        todoList.appendChild(newTodoItem);
        newTodoInput.value = ''; // Clear input field
      }
    });
  </script>
</body>
</html>
