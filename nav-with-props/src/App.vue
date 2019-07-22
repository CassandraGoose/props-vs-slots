<template>
  <div id="app">
    <Navigation :icon="gradesOrStudent" :links="classesOrStudents"/>
  </div>
</template>

<script>
import Navigation from './components/Navigation.vue'
import gradeIcon from './assets/grades.png';
import studentIcon from './assets/students.png';

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
    Navigation
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
  color: #2c3e50;
  margin-top: 60px;
}
</style>
