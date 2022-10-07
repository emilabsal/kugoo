<template>
  <div class="categories container">
    <div class="categories-top">
      <h2 class="categories-title title">Популярные категории</h2>
    </div>
    <div class="categories-block">
      <category
        title="Робот-пылесосы"
        price="29 900"
        v-for="(item, index) in 8"
        :key="index"
      />
    </div>

    <ui-button class="categories-more md" name="Смотреть все" />
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.categories {
  margin-bottom: 100px;
}

.categories-block {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 30px;
}

.categories-top {
  margin-bottom: 68px;
}

.categories-title {
  text-transform: uppercase;
}

.categories-more {
  margin: 0 auto;
  margin-top: 50px;
  padding: 15px 25px;
  background-color: transparent !important;
  color: $purple !important;
}
</style>