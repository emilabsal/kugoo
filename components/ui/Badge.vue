<template>
  <div :class="`badge ${round ? 'round' : 'square'}`">
    {{ name }}
  </div>
</template>

<script>
export default {
  props: {
    name: String,
  },
};
</script>

<style lang="scss" scoped>
.round {
  border-radius: 50%;
}

.square {
  border-radius: 5px;
}
</style>