<template>
  <nav class="navigation">
    <slot name="logo"></slot>
    <slot></slot>
  </nav>
</template>

<script>

export default {
  name: 'navigation',
}
</script>

<style>
.navigation {
  display: flex;
  justify-content: space-around;
  align-items: center;
}
</style>
