---
title: "Making a React ToDo App and Deploying it in Vercel"
seoTitle: "Making a React ToDo App and Deploying it in Vercel"
seoDescription: "To create a ToDo app with CRUD functionality using Reactjs, you can follow this article. We will also deploy our app in Vercel after making it."
datePublished: Wed Dec 21 2022 10:07:21 GMT+0000 (Coordinated Universal Time)
cuid: clkazobds000809jwe7rt7f5q
slug: making-a-react-todo-app-and-deploying-it-in-vercel
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1689847211619/e890d53d-52a6-48d1-97c4-05ee4c2a54e3.png
tags: javascript, reactjs, todoapp, vercel

---

Making a ToDo app is one of the easiest ways to learn CRUD operations. CRUD means Create, Read, Update, Delete. To create a ToDo app with CRUD functionality using Reactjs, you can follow the steps below. We will also deploy our app in Vercel after making it. Let's start.

## Step 1: Set up a new React app

1. Open your terminal and navigate to the directory where you want to create your app.
    
2. Run the following command to create a new React app:
    
    ```bash
    npx create-react-app todo-app
    ```
    
3. Navigate into the new project directory:
    
    ```bash
    cd todo-app
    ```
    
4. Start the development server:
    
    ```bash
    npm start
    ```
    
    This will open your app in the browser at [`http://localhost:3000`](http://localhost:3000).
    

## Step 2: Create necessary components and styles

1. Open the `src/App.js` file and replace its content with the following code:
    

```jsx
import React, { useState } from 'react';
import './App.css';

const App = () => {
  const [todos, setTodos] = useState([]);
  const [newTodo, setNewTodo] = useState('');

  const handleInputChange = (e) => {
    setNewTodo(e.target.value);
  };

  const handleAddTodo = () => {
    if (newTodo.trim() !== '') {
      const todo = {
        id: todos.length + 1,
        title: newTodo,
      };
      setTodos([...todos, todo]);
      setNewTodo('');
    }
  };

  const handleDeleteTodo = (id) => {
    const updatedTodos = todos.filter((todo) => todo.id !== id);
    setTodos(updatedTodos);
  };

  return (
    <div className="app">
      <h1>Todo App</h1>
      <div className="todo-form">
        <input
          type="text"
          placeholder="Enter a new todo"
          value={newTodo}
          onChange={handleInputChange}
        />
        <button onClick={handleAddTodo}>Add Todo</button>
      </div>
      <ul className="todo-list">
        {todos.map((todo) => (
          <li key={todo.id}>
            {todo.title}
            <button onClick={() => handleDeleteTodo(todo.id)}>Delete</button>
          </li>
        ))}
      </ul>
    </div>
  );
};

export default App;
```

1. Open the `src/App.css` file and replace its content with the following code:
    

```css
.app {
  background: #209cee;
  height: 100vh;
  padding: 30px;
}

.todo-form {
  margin-bottom: 10px;
}

.todo-list {
  background: #e8e8e8;
  border-radius: 4px;
  max-width: 400px;
  padding: 5px;
}

.todo {
  align-items: center;
  background: #fff;
  border-radius: 3px;
  box-shadow: 1px 1px 1px rgba(0, 0, 0, 0.15);
  display: flex;
  font-size: 12px;
  justify-content: space-between;
  margin-bottom: 6px;
  padding: 3px 10px;
}
```

## Step 3: Deploy the app on Vercel

1. Make sure you have the Vercel CLI installed. If not, you can install it globally by running:
    
    ```bash
    npm install -g vercel
    ```
    
2. Build the production version of your app by running the following command:
    
    ```bash
    npm run build
    ```
    
3. In the project directory, run the following command to deploy your app to Vercel:
    
    ```bash
    vercel --prod
    ```
    
4. Follow the prompts and provide your Vercel account credentials if requested.
    
5. After the deployment is successful, you will receive a URL for your deployed app.
    

That's it! You have now created a todo app with CRUD functionality using React.js and deployed it on Vercel. You can access your app using the provided URL.

Please note that this is a simplified implementation, and you can further enhance the app by adding update functionality (editing todos) and integrating a backend API for storing todo data persistently.

## References

1. How To Build a React To-Do App with React Hooks
    
2. How to Build a TodoApp using ReactJS, NextJS, and Supabase
    
3. How to build a React CRUD todo app (create/read todos)