<template>
  <label class="label">
    <span class="label-title" v-if="label">{{ label }}</span>
    <input
      :class="`input sm ${noBorders ? 'no-borders' : ''}`"
      type="text"
      :placeholder="placeholder"
      :style="`max-width: ${maxWidth}px`"
    />
  </label>
</template>

<script>
export default {
  props: {
    label: String,
    placeholder: String,
    maxWidth: Number,
    noBorders: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style lang="scss" scoped>
.label {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  width: 100%;
  flex-grow: 1;
}

.input {
  outline: none;
  width: 100%;
  height: 100%;
  flex-grow: 1;
}

.no-borders {
  border: 0;
}
</style>