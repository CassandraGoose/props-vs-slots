<template>
  <nav class="navigation">
    <div v-if="!isTeacher">
      <SchoolLogo />
    </div>
    <div v-if="isTeacher">
      <img :src="teacherLogo"/>
    </div>
    <div v-for="item in links" :key="item">
      <a href="google.com"><img class="icon" :src="icon"/>{{ item }}</a>
    </div>
    <select v-if="isTeacher">
      <option selected disabled>Change View</option>
      <option>Classes</option>
      <option>Grade Level</option>
      <option>Student Names</option>
    </select>
  </nav>
</template>

<script>
import SchoolLogo from './SchoolLogo.vue';
import teacherLogo from '../assets/teacher.png';

export default {
  name: 'navigation',
  data() {
    return {
      teacherLogo,
    }
  },
  props: ['links', 'icon', 'isTeacher'],
  components: {
    SchoolLogo,
  }
}
</script>

<style>
.navigation {
  display: flex;
  justify-content: space-around;
  align-items: center;
}

a {
  display: flex;
  align-items: center;
}

.icon {
  width: 25px;
  height: auto;
}
</style>
