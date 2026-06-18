<script setup lang="ts">
type Stat = {
  label: string
  value: string
  detail: string
}

defineProps<{
  stat: Stat
}>()
</script>

<template>
  <article class="stat-card">
    <p>{{ stat.label }}</p>
    <strong>{{ stat.value }}</strong>
    <span>{{ stat.detail }}</span>
  </article>
</template>
