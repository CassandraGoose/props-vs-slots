<template>
  <div>
    <Navigation :links="students" :icon="studentsIcon" :isTeacher="isTeacher"/>
    <div>
      <h3>I'm a guardian and I can see my kids' grades here.</h3>
    </div>
  </div>
</template>
<script>
import Navigation from './Navigation.vue';
import studentsIcon from '../assets/students.png';

export default {
  name: 'GuardianView',
  props: ['isTeacher'],
  data() {
    return {
      students: ['Bob', 'Jenny', 'Ty'],
      studentsIcon,
    }
  },
  components: {
    Navigation,
  },
}
</script>
