<script setup lang="ts">
defineProps<{
  title: string
  subtitle: string
}>()
</script>

<template>
  <header class="site-header">
    <div>
      <p class="eyebrow">Props Practice</p>
      <h1>{{ title }}</h1>
      <p>{{ subtitle }}</p>
    </div>
  </header>
</template>
