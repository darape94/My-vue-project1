<script setup lang="ts">
import type { Task } from "../types/task";

defineProps<{
  task: Task;
}>();
</script>

<template>
  <div class="task-card">
    <h3>{{ task.title }}</h3>
    <p>{{ task.description }}</p>
    <small>Status: {{ task.status }}</small><br />
    <small>Priority: {{ task.priority }}</small>
  </div>
</template>

<style scoped>
.task-card {
  border: 1px solid #ddd;
  padding: 16px;
  margin-bottom: 12px;
}
</style>
