<template>
  <button
    @click="$emit('button-click')"
    v-if="!link"
    :class="`button ${size} ${reverse ? 'reverse' : ''} ${
      transparent ? 'transparent' : ''
    }`"
    :style="
      !custom
        ? !transparent
          ? `background: ${
              background && !outline ? background : purple
            }; color: ${color || white}; border: 1px solid ${
              outline ? outline : background ? background : purple
            }`
          : `background: transparent; border: 0; color: ${color || black}`
        : ''
    "
  >
    <ui-icon
      :name="icon"
      :width="width"
      :height="height"
      :fill="fill"
      v-if="icon"
    />
    {{ name }}
  </button>
  <nuxt-link
    v-else
    :to="link"
    :class="`button ${size} ${reverse ? 'reverse' : ''} ${
      transparent ? 'transparent' : ''
    }`"
    :style="
      !transparent
        ? `background: ${
            background && !outline ? background : purple
          }; color: ${color || white}; border: 1px solid ${
            outline ? outline : background ? background : purple
          }`
        : `background: transparent; border: 0; color: ${color || black}`
    "
  >
    <ui-icon
      :name="icon"
      :width="width"
      :height="height"
      :fill="fill"
      v-if="icon"
    />
    {{ name }}
  </nuxt-link>
</template>

<script>
import colors from "~/assets/styles/components/_variables.scss";

export default {
  props: {
    name: String,
    link: String,
    icon: String,
    width: Number,
    height: Number,
    fill: String,
    background: String,
    color: String,
    size: String,
    reverse: Boolean,
    custom: {
      type: Boolean,
      default: false,
    },
    transparent: {
      type: Boolean,
      default: false,
    },
    outline: {
      type: Boolean,
      default: false,
    },
  },
  data() {
    return {
      purple: colors.purple,
      white: colors.white,
      black: colors.black,
    };
  },
};
</script>

<style lang="scss" scoped>
.button {
  outline: none;
  cursor: pointer;
  user-select: none;
  border-radius: 5px;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 13px;
}

.small {
  padding: 0 20px;
  min-height: 32px;
}

.medium {
  padding: 0 20px;
  font-size: 12px;
  font-weight: 400;
  line-height: 17px;
  min-height: 40px;
}

.large {
  padding: 15px 25px;
  font-size: 16px;
  font-weight: 400;
  line-height: 23px;
}

.transparent {
  padding: 0;
}

.reverse {
  flex-direction: row-reverse;
}
</style>