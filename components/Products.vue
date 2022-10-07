<template>
  <div class="products container">
    <h1 class="products-title title">Самокаты</h1>
    <div class="products-block">
      <product-mini />
      <product-mini />
      <product-mini />
      <product-mini />
      <product-mini />
      <product-mini />
      <product-mini />
      <product-mini />
    </div>
    <ui-button class="products-more md" name="Смотреть все" />
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.products-title {
  margin-bottom: 50px;
}

.products-block {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 30px;
}

.products-more {
  margin: 0 auto;
  margin-top: 50px;
  padding: 15px 25px;
  background-color: transparent !important;
  color: $purple !important;
}
</style>