<template>
  <div class="select">
    <ui-button
      class="select-button"
      icon="chevron-fill-down"
      name="Везде"
      :background="background"
      :color="black"
      :reverse="true"
    />
  </div>
</template>

<script>
import colors from "~/assets/styles/components/_typography.scss";

export default {
  props: {
    name: String,
  },
  data() {
    return {
      background: colors.background,
      black: colors.black,
    };
  },
};
</script>

<style lang="scss" scoped>
.select-button {
  padding: 6px 14px;
  font-size: 14px;
  font-weight: 400;
  line-height: 20px;
}
</style>