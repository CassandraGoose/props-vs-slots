<template>
  <div id="app">
    <div v-if="!isTeacher">
      <GuardianView :isTeacher="isTeacher" />
    </div>
    <div v-if="isTeacher">
      <TeacherView :isTeacher="isTeacher" />
    </div>
  </div>
</template>

<script>
import GuardianView from './components/GuardianView.vue';
import TeacherView from './components/TeacherView.vue';

export default {
  name: 'app',
  data() {
    return {
      isTeacher: true,
    }
  },
  components: {
    GuardianView,
    TeacherView,
  },
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
</style>
