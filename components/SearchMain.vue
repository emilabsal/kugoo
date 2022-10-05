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
    <ui-button class="search-button" icon="search" :custom="true" />
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
  border: 1.5px solid $purple;
  border-top-left-radius: 4px;
  border-bottom-left-radius: 4px;
  border-right: 0;
  display: flex;
  padding: 2.5px;
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
  background-color: $purple;
  width: 40px;
  border: 1px solid $purple;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>