<template>
  <div class="products container">
    <h1 class="products-title title">Самокаты</h1>
    <div class="products-block">
      <product-mini />
      <product-mini />
      <product-mini />
      <product-mini />
    </div>
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
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 30px;
}
</style>