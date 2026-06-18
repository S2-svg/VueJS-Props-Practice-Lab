<script setup lang="ts">
import StatCard from './StatCard.vue'

type Stat = {
  label: string
  value: string
  detail: string
}

defineProps<{
  stats: Stat[]
}>()
</script>

<template>
  <section class="panel">
    <h2>Learning Stats</h2>

    <div class="card-grid">
      <StatCard v-for="stat in stats" :key="stat.label" :stat="stat" />
    </div>
  </section>
</template>
