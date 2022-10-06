<template>
  <div :class="`badge ${round ? 'round' : 'square'}`">
    {{ name }}
  </div>
</template>

<script>
export default {
  props: {
    name: String,
    round: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style lang="scss" scoped>
.badge {
  display: inline-block;
}

.round {
  border-radius: 50%;
}

.square {
  border-radius: 5px;
}
</style>