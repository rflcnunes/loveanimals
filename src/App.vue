<template>
  <div id="app">
    <TheNavbar />
  </div>
</template>

<script>
import TheNavbar from './components/molecules/TheNavbar.vue';

export default {
  name: 'App',
  components: {
    TheNavbar
}
}
</script>

<style lang="scss">
* {
  padding: 0;
  margin: 0;
  font-family: 'Manrope', sans-serif;
  font-weight: 700;
}
</style>
