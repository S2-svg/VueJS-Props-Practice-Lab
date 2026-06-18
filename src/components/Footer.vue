<script setup lang="ts">
defineProps<{
  courseTitle: string
}>()
</script>

<template>
  <footer class="site-footer">
    <p>{{ courseTitle }} - Built with Vue props</p>
  </footer>
</template>
