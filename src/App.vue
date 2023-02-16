<template>
  <div id="app">
    <TheNavbar />
    <div id="body">
      <div class="body_the_banner">
        <TheBanner />
        <div class="description">
          <div class="hour">
            <TheIconSvg icon="hourIcon" />
            <div class="text_group">
              <TheTypography class="text" weight="bold" text="Open Everyday" />
              <TheTypography class="text" text=" 08.00 AM - 09.00PM" />
            </div>
          </div>
          <div class="address">
            <TheIconSvg icon="placeIcon" />
            <TheTypography
              class="text"
              text="Suptomo St. I45, Loren Village "
            />
          </div>
        </div>
      </div>
      <div class="body_the_image">
        <img class="body_image" src="./assets/animalsBg.svg" alt="animals_bg" />
      </div>
    </div>
    <TheFooter />
  </div>
</template>

<script>
import TheIconSvg from "./components/atoms/TheIconSvg.vue";
import TheTypography from "./components/atoms/TheTypography.vue";
import TheBanner from "./components/molecules/TheBanner.vue";
import TheFooter from "./components/molecules/TheFooter.vue";
import TheNavbar from "./components/molecules/TheNavbar.vue";

export default {
  name: "App",
  components: {
    TheNavbar,
    TheBanner,
    TheTypography,
    TheIconSvg,
    TheFooter
},
};
</script>

<style lang="scss">
* {
  padding: 0;
  margin: 0;
  font-family: "Manrope", sans-serif;
  font-weight: 700;
}

#app {
  #body {
    display: grid;
    grid-template-columns: 1fr 1fr;

    .body_the_banner {
      padding: 0 0 0 80px;
      display: grid;
      align-items: center;

      .description {
        display: grid;
        grid-auto-flow: row;
        grid-gap: 15px;

        .hour,
        .address {
          display: grid;
          grid-template-columns: 0.1fr 2fr;
          align-items: center;

          .text {
            color: $primaryGray;
          }
        }

        .text_group {
          display: flex;

          .text {
            margin: 0 5px 0 0;
          }
        }
      }
    }

    .body_the_image {
      .body_image {
        width: 90%;
        display: flex;
        align-items: center;
        margin: 0 auto;
      }
    }
  }
}
</style>
