<script setup lang="ts">
type Assignment = {
  title: string
  dueDate: string
  status: string
  points: number
}

defineProps<{
  assignment: Assignment
}>()
</script>

<template>
  <article class="assignment-card">
    <div>
      <h3>{{ assignment.title }}</h3>
      <p>Due {{ assignment.dueDate }}</p>
    </div>

    <div class="assignment-meta">
      <span>{{ assignment.status }}</span>
      <strong>{{ assignment.points }} pts</strong>
    </div>
  </article>
</template>
