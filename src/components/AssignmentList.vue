<script setup lang="ts">
import AssignmentCard from './AssignmentCard.vue'

type Assignment = {
  title: string
  dueDate: string
  status: string
  points: number
}

defineProps<{
  assignments: Assignment[]
}>()
</script>

<template>
  <section class="panel">
    <h2>Assignments</h2>

    <div class="stack">
      <AssignmentCard
        v-for="assignment in assignments"
        :key="assignment.title"
        :assignment="assignment"
      />
    </div>
  </section>
</template>
