<template>
  <div id="app">
    <div v-if="!isTeacher">
      <GuardianView />
    </div>
    <div v-if="isTeacher">
      <TeacherView />
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
      isTeacher: false,
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
