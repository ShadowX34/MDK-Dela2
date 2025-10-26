<template>
  <div class="app-container">
    <h1 class="app-title">Список дел</h1>

    <div class="tasks">
      <TaskItem
        v-for="task in tasks"
        :key="task.id"
        :task="task"
      />
    </div>
  </div>
</template>

<script setup lang="ts">
import TaskItem from './components/TaskItem.vue';

interface Task {
  id: string;
  title: string;
  text: string;
}

const tasks: Task[] = [
  { id: "1", title: "Купить продукты", text: "Молоко, хлеб, яйца" },
  { id: "2", title: "Записаться на тренировку", text: "В фитнес-зал на 18:00" },
  { id: "3", title: "Подготовить отчет", text: "Отправить начальнику до пятницы" },
  { id: "4", title: "Позвонить другу", text: "Обсудить планы на выходные" }
];
</script>

<style>
body {
  margin: 0;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background-color: #f5f7fa;
}

.app-container {
  max-width: 600px;
  margin: 0 auto;
  padding: 20px;
}

.app-title {
  text-align: center;
  color: #2c3e50;
  margin-bottom: 30px;
}

.tasks {
  display: flex;
  flex-direction: column;
  gap: 16px;
}
</style>