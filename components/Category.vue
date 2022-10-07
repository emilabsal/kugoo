<template>
  <nuxt-link class="category" to="/">
    <div class="category-desc">
      <span class="category-title lg-medium">{{ title }}</span>
      <p class="category-text sm-medium">от {{ price }} ₽</p>
    </div>
  </nuxt-link>
</template>

<script>
export default {
  props: {
    title: String,
    price: String,
  },
};
</script>

<style lang="scss" scoped>
.category {
  min-height: 255px;
  border-radius: 10px;
  background: url("~/assets/img/category/cat1.png") no-repeat center/cover;
  padding: 12px 10px;
  display: flex;
  align-items: flex-end;
  text-decoration: none;
}

.category-desc {
  background: rgba($black, 0.2);
  backdrop-filter: blur(5px);
  border-radius: 10px;
  width: 100%;
  padding: 10px 16px;
  border: 1px solid rgba($white, 0.1);
}

.category-title {
  color: $white;
  margin-bottom: 20px;
}

.category-text {
  color: $white;
}
</style>