<script setup lang="ts">
type Activity = {
  time: string
  title: string
  description: string
}

defineProps<{
  activity: Activity
}>()
</script>

<template>
  <article class="activity-item">
    <time>{{ activity.time }}</time>
    <div>
      <h3>{{ activity.title }}</h3>
      <p>{{ activity.description }}</p>
    </div>
  </article>
</template>
