<template>
  <main>
    <div class="benefits container">
      <div class="benefits-cards">
        <div class="benefits-card">
          <h3 class="benefits-title subtitle">Гарантия 1 год</h3>
          <p class="md">на весь ассортимент</p>
        </div>
        <div class="benefits-card">
          <h3 class="benefits-title subtitle">Рассрочка</h3>
          <p class="md">от 6 месяцев</p>
        </div>
        <div class="benefits-card">
          <h3 class="benefits-title subtitle">Подарки</h3>
          <p class="md">и бонусам к покупкам</p>
        </div>
      </div>
      <div class="yandex-feed">
        <img src="~/assets/img/yandex.svg" alt="yandex" />
        <div class="yandex-feed-desc">
          <span class="yandex-feed-text xs">Яндекс отзывы</span>
          <div class="yandex-feed-rating">
            <ui-icon name="star" />
            <span class="yandex-feed-rating-text subtitle">4,9</span>
          </div>
        </div>
      </div>
    </div>
    <products />
  </main>
</template>

<script>
export default {
  name: "IndexPage",
};
</script>

<style lang="scss" scoped>
.benefits {
  padding-top: 39px;
  padding-bottom: 50px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.benefits-title {
  text-transform: uppercase;
}

.yandex-feed {
  padding-top: 10px;
  padding-right: 10px;
  border-radius: 5px;
  border: 1px solid rgba(93, 108, 123, 0.1);
  display: flex;
}

.benefits-cards {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 20px;
  max-width: 724px;
  width: 100%;
}

.yandex-feed-text {
  color: $gray600;
}
</style>
