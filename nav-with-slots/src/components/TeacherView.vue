<template>
  <div>
    <Navigation>
      <template v-slot:logo><img class="logo" :src="teacherIcon"></template>
      <template>
        <div v-for="className in classes" :key="className">
          <a href="google.com"><img class="icon" :src="gradesIcon"/>{{className}}</a>
        </div>
      </template>
    </Navigation>
    <div>
      <h3>I'm a teacher and I will grade my students here.</h3>
    </div>
  </div>
</template>
<script>
import Navigation from './Navigation.vue';
import gradesIcon from '../assets/grades.png';
import teacherIcon from '../assets/teacher.png';

export default {
  name: 'TeacherView',
  data() {
    return {
      classes: ['Art History', 'Modern Art Appreciation', 'Ceramics 2'],
      gradesIcon,
      teacherIcon,
    }
  },
  components: {
    Navigation,
  }
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

