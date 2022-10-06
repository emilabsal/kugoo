<template>
  <div class="product">
    <div class="product-top">
      <div class="product-over">
        <ui-badge class="product-badge" name="ХИТ" />
        <ui-button class="product-compare" icon="balance" :custom="true" />
      </div>
      <img src="~/assets/img/scooter.png" alt="scooter" />
    </div>
    <div class="desc">
      <span class="desc-title lg-medium">Kugoo Kirin M4</span>
      <div class="data">
        <div class="data-card">
          <ui-icon name="accumulator" />
          <span class="data-card-title sm">2000 mAh</span>
        </div>
        <div class="data-card">
          <ui-icon name="power" />
          <span class="data-card-title sm">1,2 л.с.</span>
        </div>
        <div class="data-card">
          <ui-icon name="speed" />
          <span class="data-card-title sm">60 км/ч</span>
        </div>
        <div class="data-card">
          <ui-icon name="timer" />
          <span class="data-card-title sm">5 часов</span>
        </div>
      </div>
      <div class="value">
        <div class="price">
          <span class="price-old xs-medium">39 900 ₽</span>
          <span class="price-current xl">29 900 ₽</span>
        </div>
        <div class="action">
          <ui-button
            class="action-button"
            icon="cart"
            :fill="purple"
            :custom="true"
          />
          <ui-button
            class="action-button"
            icon="favor"
            :fill="purple"
            :custom="true"
          />
        </div>
      </div>
      <ui-button class="cart xs" name="Купить в 1 клик" />
    </div>
  </div>
</template>

<script>
import colors from "~/assets/styles/components/_variables.scss";
import axios from "axios";

export default {
  data() {
    return {
      purple: colors.purple,
    };
  },
  async fetch() {
    await axios.get("http://localhost:5000").then((res) => {
      console.log(res.data);
    });
  },
};
</script>

<style lang="scss" scoped>
.product {
  border-radius: 10px;
  border: 1px solid #eaebed;
  overflow: hidden;
}

.product-top {
  position: relative;
  background-color: #f0f1f5;
  display: flex;
  align-items: center;
  justify-content: center;
  padding-top: 27px;
  width: 100%;
  padding-bottom: 27px;
}

.product-over {
  position: absolute;
  top: 10px;
  left: 10px;
  width: calc(100% - 20px);
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.product-badge {
  padding: 4px 9px;
  color: $white;
  background-color: $red;
}
.product-compare {
  width: 35px;
  height: 35px;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 50%;
  border: none;
  background-color: rgba($white, 0.2);
  backdrop-filter: blur(2.5px);
}

.desc {
  padding: 20px 24px;
}

.desc-title {
  display: inline-block;
  font-weight: 600;
  margin-bottom: 20px;
}

.data {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(93px, 1fr));
  column-gap: 24px;
  row-gap: 16px;
  margin-bottom: 26px;
}

.data-card {
  display: flex;
  align-items: center;
  gap: 10px;
}

.value {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 16px;
}

.price {
  display: inline-flex;
  flex-direction: column;
  align-items: flex-start;
}

.price-old {
  color: $gray600;
}

.price-current {
  font-weight: 600;
}

.action {
  display: flex;
  gap: 10px;
  align-items: center;
}
.action-button {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  border: 1px solid $gray200;
  background-color: transparent;
  flex-shrink: 0;
}

.cart {
  width: 100%;
  padding: 10px;
  text-align: center;
}
</style>