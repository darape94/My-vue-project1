<script setup lang="ts">
import type { Task } from "../types/task";

const tasks: Task[] = [
  {
    id: 1,
    title: "Design dashboard UI",
    description: "Create layout and components",
    status: "In Progress",
    priority: "High",
  },
];
</script>

<template>
  <section>
    <h2>Dashboard</h2>

    <ul>
      <li v-for="task in tasks" :key="task.id">
        <strong>{{ task.title }}</strong>
        — {{ task.status }} ({{ task.priority }})
      </li>
    </ul>
  </section>
</template>
