<template>
  <div class="task-item">
    <h3>{{ task.title }}</h3>
    <p>{{ task.text }}</p>
  </div>
</template>

<script setup lang="ts">
import { PropType } from 'vue';

interface Task {
  id: string;
  title: string;
  text: string;
}

defineProps({
  task: {
    type: Object as PropType<Task>,
    required: true
  }
});
</script>

<style scoped>
.task-item {
  border: 1px solid #ccc;
  padding: 12px;
  border-radius: 4px;
  background-color: #f9f9f9;
}
.task-item h3 {
  margin: 0 0 8px 0;
  font-size: 1.2em;
}
.task-item p {
  margin: 0;
  color: #555;
}
</style>