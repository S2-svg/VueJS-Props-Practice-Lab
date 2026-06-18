<script setup lang="ts">
type Student = {
  name: string
  role: string
  avatar: string
  email: string
  location: string
}

defineProps<{
  student: Student
}>()
</script>

<template>
  <section class="panel">
    <h2>Student Profile</h2>

    <div class="profile">
      <div class="avatar">{{ student.avatar }}</div>
      <div>
        <h3>{{ student.name }}</h3>
        <p>{{ student.role }}</p>
      </div>
    </div>

    <ul class="simple-list">
      <li>{{ student.email }}</li>
      <li>{{ student.location }}</li>
    </ul>
  </section>
</template>
