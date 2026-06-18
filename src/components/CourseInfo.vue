<script setup lang="ts">
defineProps<{
  title: string
  instructor: string
  duration: string
  level: string
}>()
</script>

<template>
  <section class="panel">
    <h2>Course Information</h2>

    <div class="info-grid">
      <p>
        <span>Course</span>
        {{ title }}
      </p>
      <p>
        <span>Instructor</span>
        {{ instructor }}
      </p>
      <p>
        <span>Duration</span>
        {{ duration }}
      </p>
      <p>
        <span>Level</span>
        {{ level }}
      </p>
    </div>
  </section>
</template>
