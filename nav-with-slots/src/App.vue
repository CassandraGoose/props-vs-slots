<template>
  <div id="app">
    <Navigation>
      <template v-slot:logo><SchoolLogo /></template>
      <template v-slot:links>
        <div v-for="link in classesOrStudents" :key="link">
          <a href="google.com"><img class="icon" :src="gradesOrStudent" />{{link}}</a>
        </div>
      </template>
    </Navigation>
  </div>
</template>

<script>
import Navigation from './components/Navigation.vue'
import gradeIcon from './assets/grades.png';
import studentIcon from './assets/students.png';
import SchoolLogo from './components/SchoolLogo.vue';

export default {
  name: 'app',
  data() {
    return {
      user: {
        isAdvisor: false,
      }
    }
  },
  components: {
    Navigation,
    SchoolLogo,
  },
  computed: {
    classesOrStudents() {
      return this.user.isAdvisor ? ['Art History', 'Modern Art Appreciation', 'Ceramics 2'] : ['Jeff', 'Jim', 'Bobbert'];
    },
    gradesOrStudent() {
      return this.user.isAdvisor ? gradeIcon : studentIcon;
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
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
