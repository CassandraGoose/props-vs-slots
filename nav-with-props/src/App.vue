<template>
  <div id="app">
    <div v-if="!isAdvisor">
      <GuardianView />
    </div>
    <div v-if="isAdvisor">
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
      isAdvisor: true,
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
