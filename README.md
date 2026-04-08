# React Temporal Task System

A React-based task system focused on **temporal state flow and history tracking**.

This project explores state as a **time-based structure**, enabling undo/redo functionality through a history stack model.

---

## Key Features

- Custom hook architecture (extensible design)
- State history (undo / redo)
- Temporal UI rendering (state changes over time)
- Immutable state transitions
- Centralized state control

---

## Project Structure

src/
├── components/
│ ├── Todos.jsx # Main state container
│ ├── TodosForm.jsx # Input component
│ └── TodoItem.jsx # Individual todo item
├── hooks/
│ └── useUndoRedo.js # (optional) custom hook for history

---

## Getting Started

### 1. Clone the repository

```bash
git clone <your-repo-url>
cd react-todo
```

### 2. Install dependencies

```bash
npm install
```

### 3. Run development server

```bash
npm run dev
```

### 4. Open in browser

http://localhost:5173

---

## Core Concept

This system treats application state as a temporal sequence, not just a static value.

State Model
past     → previous states
present  → current state
future   → redo states

State Flow
Action → past.push(present) → present updated → future cleared

### State Timeline Visualization

[ Past Stacks ]  <---  ( Present )  --->  [ Future Stacks ]
   [t-2, t-1]            [ t ]               [t+1, t+2]
      ↑                    |                    ↑
    Undo                 Current               Redo

### Core State Principles

- **Immutable State Transitions**  
  State updates are performed using React’s functional update pattern (`setState((prev) => ...)`) and the spread operator (`...`) to ensure immutability.  
  This guarantees that the original state is never mutated, preserving predictable state transitions and enabling reliable history tracking.

- **Functional Updates**  
  Functional updates are used to ensure data consistency in asynchronous environments.  
  By deriving the next state from the previous state, the system avoids race conditions and maintains a consistent state even when multiple updates are queued.

---

## Undo / Redo Logic

Undo
- Moves current state → future
- Restores last state from past

Redo
- Moves current state → past
- Restores next state from future

---

## Design Philosophy

This project is built on the idea that:

### “State is not static — it is a timeline.”

Instead of overwriting state, we preserve its evolution as a structured history.

---

## Future Improvements

Time-based navigation (timeline slider)
Persistent history (localStorage / backend)
Advanced state compression
Visualization of state transitions

---

## Author

Jungae Lee
Korea National University of Arts
jungae1000@karts.ac.kr




A React-based task system focused on temporal state flow and history tracking.

👉 GitHub Preview: https://github.com/Jung-AeLee/react-temporal-task-system

This project explores state as a time-based structure, enabling undo/redo functionality through a history stack model.

---

## ✨ Key Features

- Custom hook architecture (extensible design)
- State history (undo / redo)
- Temporal UI rendering (state changes over time)
- Immutable state transitions
- Centralized state control

---

## 🧠 Core Concept

This system treats application state as a temporal sequence, not just a static value.

Instead of simply updating state, it preserves the evolution of state over time.

---

## 🧱 Core State Principles

### Immutable State Transitions  
State updates are performed using React’s functional update pattern (`setState((prev) => ...)`) and the spread operator (`...`) to ensure immutability.  
This guarantees that the original state is never mutated, preserving predictable state transitions and enabling reliable history tracking.

### Functional Updates  
Functional updates are used to ensure data consistency in asynchronous environments.  
By deriving the next state from the previous state, the system avoids race conditions and maintains a consistent state even when multiple updates are queued.

---

## 🚀 What You Get

This project is not just a Todo app.

It demonstrates:

- A **state-driven architecture**
- A **time-aware data model**
- A foundation for **advanced UI systems (time-travel debugging, history-based apps)**

---

## 📌 Ideal For

- Developers who want to understand advanced React state patterns
- Building complex UI systems with undo/redo
- Learning how to structure state as a timeline
- Portfolio projects aiming for a deeper architectural level

---

## 💡 Why This Matters

Most applications treat state as a single snapshot.

This project treats state as a **timeline**, making it possible to:
- Move backward and forward in time
- Preserve full history
- Build more predictable and controllable systems

---

## 🔗 GitHub Repository

Full source code and preview:

👉 https://github.com/Jung-AeLee/react-temporal-task-system

