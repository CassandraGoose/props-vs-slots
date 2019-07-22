<template>
  <nav class="navigation">
    <SchoolLogo />
    <div v-for="item in links" :key="item">
      <a href="google.com"><img class="icon" :src="icon"/>{{ item }}</a>
    </div>
  </nav>
</template>

<script>
import SchoolLogo from './SchoolLogo.vue';

export default {
  name: 'navigation',
  data() {
    return {}
  },
  props: ['links', 'icon'],
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
