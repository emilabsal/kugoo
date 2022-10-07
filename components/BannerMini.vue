<template>
  <div class="banner">
    <div class="banner-desc">
      <div class="banner-desc-top">
        <span class="banner-title subtitle">Подбор модели электросамоката</span>
        <p class="banner-text md">
          Пройдите тест и выберите электросамокат по своим критериям
        </p>
      </div>
      <ui-button
        class="banner-link sm-medium"
        to="/"
        name="Подобрать модель"
        icon="arrow-right"
        :fill="purple"
        :reverse="true"
        :transparent="true"
      />
    </div>
    <img src="~/assets/img/bannerMini/banner-scooter.png" alt="banner" />
  </div>
</template>

<script>
import colors from "~/assets/styles/components/_variables.scss";

export default {
  data() {
    return {
      purple: colors.purple,
    };
  },
};
</script>

<style lang="scss" scoped>
.banner {
  border-radius: 10px;
  overflow: hidden;
  display: flex;
  justify-content: space-between;
  background-color: $background;
}

.banner-desc {
  padding: 32px 40px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
}

.banner-title {
  display: inline-block;
  font-weight: 600 !important;
  text-transform: uppercase;
  margin-bottom: 10px;
}

.banner-link {
  color: $purple !important;
}
</style>