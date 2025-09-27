# Stack-based-Text-Editor
Stack-based Text Editor using C++ – A console-based text editor built with singly linked lists and stacks to perform line-based editing with Undo/Redo functionality. 
# 📄 Stack-Based Text Editor

---

## 📚 Background

Text editing is an essential part of digital tasks like coding, writing, and composing emails. In modern editors, **Undo** and **Redo** functionality is crucial — it helps users revert mistakes or repeat changes efficiently.

This project implements a **stack-based text editor**, where each operation (insert, delete, replace) is stored in a stack, enabling users to undo or redo actions by simply popping and pushing these operations. 

Such systems are particularly useful when working with long documents or code, where frequent changes are made.

---

## 🧩 Problem Statement

The goal is to design a simple but efficient text editor that:

- Supports **Insert**, **Delete**, and **Replace** operations
- Allows **Undo** and **Redo** functionality
- Saves the current document to an external `.txt` file
- Clears all text content when needed

Traditional approaches using arrays/lists can be memory-heavy and inefficient for Undo/Redo. This project uses **Stacks** and **Linked Lists** to improve performance and maintain simplicity.

---

## 🎯 Objectives

- Undo the most recent change
- Redo an undone change
- Efficiently manipulate lines using Linked List
- Save current content to a `.txt` file
- Provide a simple, user-friendly console interface

---

## 🧠 Data Structures Used

### 🔗 Linked List
- Stores each line as a node
- Allows fast insertions/deletions at head, tail, or any position

### 🥞 Stacks (Undo & Redo)
- **Undo Stack**: Stores previous actions with line number, operation type, and text
- **Redo Stack**: Stores undone actions that can be reapplied

---

## 🚀 Features

| Feature         | Description |
|-----------------|-------------|
| Insert Text     | Add text at any specific line (start, middle, or end) |
| Delete Line     | Delete a specific line number |
| Replace Line    | Replace content of a specific line |
| Undo            | Revert the last operation (Insert/Delete/Replace) |
| Redo            | Redo an undone action |
| Print Lines     | Display all text lines in order |
| Save to File    | Save content to `output.txt` file |
| Clear Editor    | Delete all lines and reset the editor |

---

## ⚙️ Methodology

### 🛠 Operation Steps

- **Insert**: User enters line number and text → inserted into linked list → pushed to Undo stack
- **Delete**: User enters line number → line is removed → operation pushed to Undo stack
- **Replace**: User enters line number and new text → old text is replaced → pushed to Undo stack
- **Undo**: Most recent operation popped from Undo stack and reversed → pushed to Redo stack
- **Redo**: Most recent undone operation popped from Redo stack and reapplied → pushed back to Undo stack
- **Save**: Writes all linked list nodes (text lines) to `output.txt`
- **Clear**: Deletes all nodes from the linked list

---

## 💻 How to Run

### 🛠 Requirements:
- C++ Compiler (e.g., g++, Code::Blocks, VS Code)
==== STACK-BASED TEXT EDITOR ====
1. Insert text into Line N
2. Delete line N
3. Replace text in Line N
4. Print all lines
5. Undo
6. Redo
7. Save to .txt file
8. Clear editor
0. Exit
Enter your choice:
