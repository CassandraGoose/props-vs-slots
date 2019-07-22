<template>
  <div>
    <Navigation>
      <template v-slot:logo><SchoolLogo /></template>
      <template>
        <div v-for="student in students" :key="student">
          <a href="google.com"><img class="icon" :src="studentsIcon"/>{{student}}</a>
        </div>
      </template>
    </Navigation>
    <div>
      <h3>I'm a guardian and I can see my kids' grades here.</h3>
    </div>
  </div>
</template>
<script>
import Navigation from './Navigation.vue';
import SchoolLogo from './SchoolLogo.vue';
import studentsIcon from '../assets/students.png';

export default {
  name: 'GuardianView',
  data() {
    return {
      students: ['Bob', 'Jenny', 'Ty'],
      studentsIcon,
    }
  },
  components: {
    Navigation,
    SchoolLogo,
  },
}
</script>
<style>
  .icon {
    width: 25px;
    height: auto;
  }

  a {
    display: flex;
    align-items: center;
  }
</style>
