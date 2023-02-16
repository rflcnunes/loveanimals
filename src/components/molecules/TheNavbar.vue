<template>
  <div class="the-nav-bar">
    <div class="the-nav-bar__close">
      <TheIconSvg class="the-icon-close" size="sm" icon="close" />
    </div>
    <div class="the-nav-bar__social-media">
      <TheIconSvg size="xl" icon="facebook" />
      <TheIconSvg size="xl" icon="youtube" />
      <TheIconSvg size="xl" icon="twitter" />
    </div>
  </div>
</template>
<script>
import TheIconSvg from "../atoms/TheIconSvg.vue";

export default {
  name: "TheNavBar",
  components: {
    TheIconSvg,
  },
};
</script>
<style lang="scss">
.the-nav-bar {
  display: grid;
  grid-template-columns: 2fr 0.2fr;
  padding: 24px 30px 0 30px;

  &__close {
    .the-icon-close {
      display: flex;
      align-content: center;
      background-color: $primaryBlue;
      padding: 10px;
      border-radius: 10px;
    }
  }

  &__social-media {
    display: grid;
    grid-auto-flow: column;
    grid-gap: 29px;
    justify-content: space-between;
    align-content: center;
  }
}
</style>
