<template>
  <div class="task-item">
    <h3 class="task-title">{{ task.title }}</h3>
    <p class="task-text">{{ task.text }}</p>
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
  border: 1px solid #dcdfe6;
  padding: 16px;
  border-radius: 8px;
  background-color: white;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
  transition: box-shadow 0.2s ease;
}

.task-item:hover {
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.task-title {
  margin: 0 0 8px 0;
  font-size: 1.2em;
  color: #34495e;
}

.task-text {
  margin: 0;
  color: #7f8c8d;
  line-height: 1.5;
}
</style>