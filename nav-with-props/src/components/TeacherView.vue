<template>
  <div>
    <Navigation :links="classes" :icon="gradesIcon" />
    <div>
      <h3>I'm a teacher and I will grade my students here.</h3>
    </div>
  </div>
</template>
<script>
import Navigation from './Navigation.vue';
import gradesIcon from '../assets/grades.png';

export default {
  name: 'TeacherView',
  data() {
    return {
      classes: ['Art History', 'Modern Art Appreciation', 'Ceramics 2'],
      gradesIcon,
    }
  },
  components: {
    Navigation,
  }
}
</script>
