<template>
  <div class="search">
    <div class="search-inner">
      <ui-select />
      <ui-input
        class="search-input"
        placeholder="Искать самокат KUGO"
        :maxWidth="444"
        :noBorders="true"
      />
    </div>
    <ui-button class="search-button" icon="search" />
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.search {
  display: flex;
  align-items: center;
}
.search-inner {
  border: 2px solid $purple;
  border-radius: 4px;
  display: flex;
  padding: 4px;
}

.search-input {
  margin: 0 20px;
}

.search-input::placeholder {
  color: $gray600;
}

.search-button {
  height: 40px;
  border-top-left-radius: 0;
  border-bottom-left-radius: 0;
}
</style>