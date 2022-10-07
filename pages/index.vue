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
    <div class="banners-mini container">
      <banner-mini />
      <banner-mini />
    </div>
    <div class="drone">
      <div class="drone-inner container">
        <img class="drone-image" src="~/assets/img/drone.png" alt="drone" />
        <div class="drone-desc">
          <ui-badge class="drone-badge sm" name="Акция" />
          <span class="drone-title title"
            >Бесплатная доставка электросамокатов по России до 01.09</span
          >
          <ui-button class="drone-link md" name="Подробнее" />
        </div>
      </div>
    </div>
    <all-categories />
    <div class="dealer">
      <div class="dealer-image-block">
        <div class="dealer-test-drive">
          <span class="dealer-test-drive-title lg-medium"
            >Тест-драйв в Москве</span
          >
          <p class="dealer-test-drive-text sm">
            Оцените все преимущества самокатов лично
          </p>
          <ui-button name="Подробнее" icon="arrow-right" />
        </div>
      </div>
      <div class="dealer-desc">
        <span class="dealer-desc-title title"
          >Kugoo-Russia — первый официальный дилер Kugoo Kirin в России</span
        >
        <p class="dealer-desc-text md">
          Наша цель предоставить полный ассортимент современной продукции Kugoo
          Kirin, которая улучшает и упрощает жизнь. Стремимся подарить комфорт и
          эмоции, поэтому помогаем с выбором и внимательно относимся к
          сервисному обслуживанию.
        </p>
        <div class="dealer-get">
          <span class="dealer-get-title sm-medium"
            >Специализируемся исключительно на бренде Kugoo, поэтому вы
            получите:</span
          >
          ul.
        </div>
      </div>
    </div>
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

.banners-mini {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 30px;
  margin: 110px auto;
}

//drone
.drone {
  width: calc(100% - 60px);
  margin: 0 30px;
  background: radial-gradient(
    76.7% 707.77% at 23.3% 72.57%,
    #595959 0%,
    #3b3e46 100%
  );
  border-radius: 10px;
  position: relative;
  margin-bottom: 87px;
  overflow: hidden;
}
.drone-inner {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  gap: 10px;
}

.drone-image {
  position: absolute;
  left: 30px;
}

.drone-desc {
  max-width: 441px;
  margin: 67px 0;
}

.drone-badge {
  background-color: $red;
  color: $white;
  padding: 3px 12px;
}

.drone-title {
  text-transform: uppercase;
  color: $white;
  display: block;
  margin: 27px 0;
}

.drone-link {
  padding: 15px 25px;
  background-color: $white !important;
  color: $black !important;
}
</style>
