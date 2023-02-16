<template>
  <div class="the-footer">
    <div id="background">
      <div id="white"></div>
      <div id="blue"></div>
    </div>
    <TheTypography
      class="text"
      text="We Love Animals"
      type="secondary"
      displaySize="2xl"
    />
  </div>
</template>

<script>
import TheTypography from "../atoms/TheTypography.vue";

export default {
  name: "TheFooter",
  components: {
    TheTypography,
  },
};
</script>

<style lang="scss">
.the-footer {
  position: relative;

  #background {
    position: absolute;
    height: 100%;
    width: 100%;

    #white {
      position: absolute;
      height: 50%;
      width: 100%;
      background-color: transparent;
    }

    #blue {
      position: absolute;
      bottom: 0;
      height: 50%;
      width: 100%;
      background-color: blue;
    }
  }

  .text {
    position: relative;
    z-index: 1;
    padding: 10px;
    color: $primaryGray;
  }
}
</style>
