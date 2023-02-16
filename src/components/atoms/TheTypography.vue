<template>
  <div class="the_typography">
    <div
      id="item"
      :class="[
        `font-family-${type}`,
        `font-size-${textSize}`,
        `font-size-display-${displaySize}`,
        `font-weight-${weight}`,
        `font-${color}`,
      ]"
    >
      {{ text }}
    </div>
  </div>
</template>

<script>
export default {
  name: "TheTypography",
  props: {
    textSize: {
      type: String,
      default: "",
    },
    displaySize: {
      type: String,
      default: "",
    },
    weight: {
      type: String,
      default: "regular",
    },
    type: {
      type: String,
      default: "primary",
    },
    text: {
      type: String,
      default: "Texto padrão",
    },
    color: {
      type: String,
      default: "",
    },
  },
};
</script>

<style lang="scss" scoped>
#item {
  display: flex;
}

.font-family {
  &-primary {
    font-family: $primaryFontFamily;
  }

  &-secondary {
    font-family: $secondaryFontFamily;
  }
}

.font-size {
  &-xs {
    font-size: $fontSizeXs;
  }

  &-sm {
    font-size: $fontSizeSm;
  }

  &-md {
    font-size: $fontSizeMd;
  }

  &-lg {
    font-size: $fontSizeLg;
  }

  &-xl {
    font-size: $fontSizeXl;
  }

  &-display-xs {
    font-size: $fontSizeDisplayXs;
  }

  &-display-sm {
    font-size: $fontSizeDisplaySm;
  }

  &-display-md {
    font-size: $fontSizeDisplayMd;
  }

  &-display-lg {
    font-size: $fontSizeDisplayLg;
  }

  &-display-xl {
    font-size: $fontSizeDisplayXl;
  }

  &-display-2xl {
    font-size: $fontSizeDisplay2Xl;
  }
}

.font-weight {
  &-regular {
    font-weight: $fontWeightRegular;
  }

  &-medium {
    font-weight: $fontWeightMedium;
  }

  &-semibold {
    font-weight: $fontWeightSemibold;
  }

  &-bold {
    font-weight: $fontWeightBold;
  }
}

.font {
  &-primaryBlue {
    color: $primaryBlue;
  }
}
</style>
