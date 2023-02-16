<template>
  <div id="app">
    <TheNavbar />
    <div id="body">
      <TheBanner />
    </div>
  </div>
</template>

<script>
import TheBanner from './components/molecules/TheBanner.vue';
import TheNavbar from './components/molecules/TheNavbar.vue';

export default {
  name: 'App',
  components: {
    TheNavbar,
    TheBanner
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
