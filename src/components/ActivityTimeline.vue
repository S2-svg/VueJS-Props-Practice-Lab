<script setup lang="ts">
import ActivityItem from './ActivityItem.vue'

type Activity = {
  time: string
  title: string
  description: string
}

defineProps<{
  activities: Activity[]
}>()
</script>

<template>
  <section class="panel">
    <h2>Activity Timeline</h2>

    <div class="timeline">
      <ActivityItem v-for="activity in activities" :key="activity.title" :activity="activity" />
    </div>
  </section>
</template>
