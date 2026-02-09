<script setup lang="ts">
import TaskCard from "../components/TaskCard.vue";
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

    <TaskCard
      v-for="task in tasks"
      :key="task.id"
      :task="task"
    />
  </section>
</template>
