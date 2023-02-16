<template>
  <img :class="`icon-${size}`" :src="iconUrl" alt="icon" />
</template>

<script>
export default {
  name: "TheIconSvg",
  props: {
    icon: {
      type: String,
      required: true,
    },
    size: {
      type: String,
      default: "md",
    },
  },
  computed: {
    iconUrl() {
      return require(`@/assets/${this.icon}.svg`);
    },
  },
};
</script>

<style lang="scss" scoped>
.icon {
  &-sm {
    width: 20px;
  }

  &-md {
    width: 28px;
  }

  &-lg {
    width: 30px;
  }

  &-xl {
    width: 32px;
  }
}
</style>
