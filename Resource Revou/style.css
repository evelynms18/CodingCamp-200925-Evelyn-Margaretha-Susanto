"use strict";

document.addEventListener("DOMContentLoaded", () => {
  const form = document.getElementById("todo-form");
  const todoInput = document.getElementById("todo-input");
  const dateInput = document.getElementById("date-input");
  const todoList = document.getElementById("todo-list");
  const filterInput = document.getElementById("filter-input");

  form.addEventListener("submit", (e) => {
    e.preventDefault();
    const task = todoInput.value;
    const date = dateInput.value;

    if (!task || !date) {
      alert("Silakan pilih aktivitas dan tanggal.");
      return;
    }

    const li = document.createElement("li");
    li.innerHTML = `${task} - ${date} <button class="delete-btn">Hapus</button>`;
    todoList.appendChild(li);

    todoInput.value = "";
    dateInput.value = "";
  });

  todoList.addEventListener("click", (e) => {
    if (e.target.classList.contains("delete-btn")) {
      e.target.parentElement.remove();
    }
  });

  filterInput.addEventListener("input", () => {
    const filter = filterInput.value.toLowerCase();
    const tasks = todoList.getElementsByTagName("li");

    Array.from(tasks).forEach((task) => {
      const text = task.textContent.toLowerCase();
      task.style.display = text.includes(filter) ? "" : "none";
    });
  });
});


