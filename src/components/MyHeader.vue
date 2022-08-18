<template>
  <section>
    <div class="bourger">
      <img src="@/assets/bourger.png" />
    </div>
    <div class="header-container">
      <div class="desctop">
        <nav class="text-header">
          <div class="text-header__block">
            <li>Пациентам</li>
            <li>Бизнесу</li>
            <li>Франчайзинг</li>
            <img src="@/assets/nav.png" />
            <li>Интернет магазин</li>
            <MySelect :options="['О компании', 'Что-то еще']" />
          </div>
          <div class="header-phone_wraper">
            <img src="@/assets/v.png" />
            <MySelect
              class="text-header__phone"
              :options="['&nbsp;8 (800) 33-33-299', '+7 (495) 150-80-32']"
            />
          </div>
          <div class="text-header__block">
            <li>Адреса</li>
            <img src="@/assets/nav.png" />
            <li>Москва</li>
            <MySelect :options="['Eng', 'Ru']" />
          </div>
        </nav>
      </div>
      <div class="search-line">
        <img class="logo" src="@/assets/logo.png" />
        <MySearchInput class="search-line__search-input"/>
        <img class="search-icon desctop" src="@/assets/man.png" />
        <img class="search-icon desctop" src="@/assets/cart.png" />
        <MyButton class="desctop" :title="'Результаты'" />
      </div>
    </div>
    <div class="submenu-container tablet">
      <div class="submenu-wraper">
        <nav class="submenu">
          <li>Covid-19</li>
          <li>Анализы</li>
          <li>Медицинские услуги</li>
          <li>Запись к врачу</li>
          <li>Самодиагностика</li>
          <li>Акции</li>
          <MySelect :options="['Еще']" />
        </nav>
        <div class="submenu">
          <div class="submenu-icon">
            <img src="@/assets/describe.png" />
            <li>Расшифровка</li>
          </div>
          <div class="submenu-icon">
            <img src="@/assets/television.png" />
            <li>Телемедицина</li>
          </div>
        </div>
      </div>
    </div>
    <div class="search-input-mobi">
        <MySearchInput/>
    </div>
    <div class="crumbs-container">
      <nav class="crumbs">
        <li class="crumbs-active">Polymed</li>
        <li>&bull;</li>
        <li class="crumbs-active">Анализы</li>
        <li>&bull;</li>
        <li>Анализы при беременности</li>
      </nav>
    </div>
  </section>
</template>

<script>
import MySelect from "./UI/MySelect.vue";
import MyButton from "./UI/MyButton.vue";
import MySearchInput from "./UI/MySearchInput.vue";
export default {
  name: "my-header",
  components: { MySelect, MyButton, MySearchInput },
};
</script>

<style>
li {
  list-style-type: none;
}
.bourger {
  display: none;
  float: right;
}
.bourger img {
  height: 45px;
  width: 45px;
  margin-left: 30px;
}
.header-container {
  max-width: 1140px;
  padding-left: 30px;
  padding-right: 30px;
  margin: auto;
}
.text-header {
  display: flex;
  flex-wrap: wrap-reverse;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 120%;
  color: #1a2a45;
}
.text-header__phone {
  padding-right: 5px;
  font-family: "PT Root UI" !important;
  font-style: normal !important;
  font-weight: 500 !important;
  font-size: 20px !important;
  line-height: 120% !important;
  color: #ff1b7a !important;
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
}
.header-phone_wraper {
  display: flex;
  align-items: center;
}
.header-phone_wraper img {
  position: relative;
  z-index: -1;
  left: 165px;
  height: 8px;
  height: 7px;
}
.text-header__block {
  display: flex;
  flex-direction: row;
  align-items: center;
}
.text-header__block li {
  margin-right: 24px;
}
.text-header__block img {
  width: 11.22px;
  height: 14px;
  margin-right: 7px;
}
.search-line {
  margin-top: 30px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.logo {
  width: 170px;
  height: 42px;
  margin-right: 16px;
}
.search-input {
  display: flex;
  border: 1px solid #ff1b7a;
  width: 49%;
  height: 44px;
  border-radius: 8px;
  margin-right: 7px;
}
.submenu-container {
  background: #f7f9fe;
  margin-top: 24px;
  padding-top: 24px;
  padding-bottom: 24px;
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  align-items: center;
  width: 100%;
}
.submenu-icon {
  display: flex;
  margin-right: 24px;
  margin-bottom: 4px;
  max-height: 18px;
}
.submenu-icon img {
  height: inherit;
  margin-right: 6px;
  overflow: hidden;
}
.submenu {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  align-items: center;
}
.submenu-wraper {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 90%;
  max-width: 1140px;
}
.submenu-container li {
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 400;
  font-size: 15px;
  line-height: 120%;
  color: #1a2a45;
}
.submenu-container li:not(:last-child) {
  margin-right: 24px;
}
.crumbs-container {
  max-width: 1140px;
  padding-left: 30px;
  padding-right: 30px;
  margin: auto;
}
.crumbs {
  color: #8790ae;
  display: flex;
  flex-direction: row;
  align-items: center;
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 500;
  font-size: 12px;
  line-height: 24px;
  margin-top: 16px;
}
.crumbs li {
  margin-right: 16px;
}
.crumbs-active {
  color: #00b4ff;
}
.search-input-mobi {
  display: none;
}
@media (max-width: 990px) {
  .bourger {
    display: block;
  }
  .desctop {
    display: none;
  }
  .search-input {
    width: 100%;
  }
}
@media (max-width: 540px) {
  .tablet {
    display: none;
  }
  .search-line__search-input {
   display: none;
  }
  .search-input-mobi {
    display: flex;
    margin-left: 30px;
    margin-top: 10px;
  }
}
</style>
