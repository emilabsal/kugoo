<template>
  <header class="header">
    <div class="header-sub">
      <div class="header-sub-inner container">
        <div class="header-sub-left">
          <nav class="subnav">
            <ul class="subnav-list">
              <li class="subnav-item">
                <ui-button name="Сервис" :transparent="true" :color="gray600" />
              </li>
              <li class="subnav-item">
                <ui-button
                  name="Сотрудничество"
                  :transparent="true"
                  :color="gray600"
                />
              </li>
              <li class="subnav-item">
                <ui-button
                  name="Заказать звонок"
                  :transparent="true"
                  :color="gray600"
                />
              </li>
            </ul>
          </nav>
          <ul class="social">
            <li class="social-item">
              <ui-button icon="viber" :transparent="true" />
            </li>
            <li class="social-item">
              <ui-button icon="whatsapp" :transparent="true" />
            </li>
            <li class="social-item">
              <ui-button icon="telegram" :transparent="true" />
            </li>
          </ul>
        </div>
        <div class="header-contacts">
          <a class="header-phone button-small-medium" href="tel:88005055461"
            >+7 (800) 505-54-61</a
          >
          <ui-button icon="plus-circle" :transparent="true" />
        </div>
      </div>
    </div>
    <div class="header-main">
      <div class="header-main-inner container">
        <div class="header-main-left">
          <ui-button
            class="header-logo"
            name="KUGOO"
            :transparent="true"
            link="/"
          />
          <ui-button class="catalogue" name="Каталог" icon="catalogue" />
          <search-main />
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import colors from "~/assets/styles/components/_variables.scss";

export default {
  data() {
    return {
      gray600: colors.gray600,
    };
  },
};
</script>

<style lang="scss" scoped>
.header {
}

.header-sub {
  padding: 11px 0;
  border-bottom: 1px solid #ecf3ff;
}

.header-sub-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.header-sub-left {
  display: flex;
  align-items: center;
  gap: 30px;
}

.header-contacts {
  display: flex;
  align-items: center;
}

.subnav-list {
  display: flex;
  list-style-type: none;
  align-items: center;
  gap: 30px;
}

.subnav-item {
  display: flex;
}

.social {
  list-style-type: none;
  display: flex;
  align-items: center;
  gap: 9px;
}

.header-phone {
  text-decoration: none;
  margin-right: 9px;
}

.header-main {
  padding: 27px 0;
}

.header-logo {
  font-size: 30px;
  font-weight: 700;
  line-height: 43px;
  text-decoration: none;
}

.header-main-left {
  display: flex;
  align-items: center;
}

.catalogue {
  padding: 8px 18px;
  font-size: 16px;
  font-weight: 500;
  line-height: 23px;
  margin-left: 35px;
  margin-right: 20px;
}
</style>