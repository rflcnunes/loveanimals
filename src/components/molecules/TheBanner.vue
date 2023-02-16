<template>
  <div class="the-banner">
    <ul class="the-banner__list">
      <li
        v-for="(item, index) in items"
        :key="index"
        :class="[
          'the-banner__item',
          { 'the-banner__item--active': selectedItemIndex === index },
        ]"
        @click="selectedItemIndex = index"
      >
        <TheTypography class="item" :text="item" displaySize="xl" />
      </li>
    </ul>
  </div>
</template>

<script>
import TheTypography from '../atoms/TheTypography.vue';

export default {
    name: "TheBanner",
    data() {
        return {
            items: ["Home", "Our Service", "FAQ", "About Us"],
            selectedItemIndex: 0,
        };
    },
    mounted() {
        setInterval(() => {
            this.selectedItemIndex = (this.selectedItemIndex + 1) % this.items.length;
        }, 1000);
    },
    components: { TheTypography }
};
</script>

<style lang="scss">
.the-banner {
  font-family: $primaryFontFamily;

  &__list {
    list-style: none;
    display: grid;
    grid-auto-flow: row;
  }

  &__item {
    display: inline-block;
    margin-right: 10px;
    cursor: pointer;

    .item {
      margin-left: 14px;
    }

    &:last-child {
      margin-right: 0;
    }

    &--active {
      color: $primaryYellow;
      border-left: 5px solid $primaryYellow;
      transition: all 1s ease-out;
    }
  }
}
</style>
