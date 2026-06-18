<script setup lang="ts">
import ActivityTimeline from './components/ActivityTimeline.vue'
import AssignmentList from './components/AssignmentList.vue'
import CourseInfo from './components/CourseInfo.vue'
import Footer from './components/Footer.vue'
import Header from './components/Header.vue'
import StatsSection from './components/StatsSection.vue'
import StudentProfile from './components/StudentProfile.vue'

const course = {
  title: 'Vue.js Props Practice Lab',
  subtitle: 'Learn how parent components pass data to child components.',
  instructor: 'Savin Phuong',
  duration: '4 weeks',
  level: 'Beginner',
}

const student = {
  name: 'Maya Chen',
  role: 'Frontend Student',
  avatar: 'MC',
  email: 'maya.chen@example.com',
  location: 'Phnom Penh, Cambodia',
}

const stats = [
  { label: 'Completed Lessons', value: '12', detail: 'of 16 lessons' },
  { label: 'Average Score', value: '92%', detail: 'across all assignments' },
  { label: 'Study Streak', value: '8 days', detail: 'keep it going' },
]

const assignments = [
  {
    title: 'Create Component Props',
    dueDate: 'June 12',
    status: 'Done',
    points: 20,
  },
  {
    title: 'Render Lists With v-for',
    dueDate: 'June 15',
    status: 'In Progress',
    points: 25,
  },
  {
    title: 'Build a Student Dashboard',
    dueDate: 'June 20',
    status: 'Not Started',
    points: 35,
  },
]

const activities = [
  {
    time: '09:00',
    title: 'Joined Vue props lesson',
    description: 'Reviewed how props move data from parent to child components.',
  },
  {
    time: '11:30',
    title: 'Submitted assignment',
    description: 'Uploaded the first component practice activity.',
  },
  {
    time: '14:15',
    title: 'Received feedback',
    description: 'Instructor suggested using clearer prop names.',
  },
]
</script>

<template>
  <div class="app-shell">
    <Header :title="course.title" :subtitle="course.subtitle" />

    <main class="page-content">
      <CourseInfo
        :title="course.title"
        :instructor="course.instructor"
        :duration="course.duration"
        :level="course.level"
      />

      <StatsSection :stats="stats" />

      <div class="dashboard-grid">
        <StudentProfile :student="student" />
        <AssignmentList :assignments="assignments" />
      </div>

      <ActivityTimeline :activities="activities" />
    </main>

    <Footer :course-title="course.title" />
  </div>
</template>
