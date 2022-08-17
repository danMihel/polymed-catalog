<template>
  <section>
    <div class="header-container">
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
      <div class="search-line">
        <img class="logo" src="@/assets/logo.png" />
        <div class="search-input">
          <input
            class=" "
            type="search"
            placeholder="Быстрый поиск нужного исследования..."
          />
          <img class="search-btn" src="@/assets/Search-icon.png" />
        </div>
        <img class="search-icon" src="@/assets/man.png" />
        <img class="search-icon" src="@/assets/cart.png" />
        <MyButton :title="'Результаты'" />
      </div>
    </div>
    <div class="submenu-container">
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
          <img src="@/assets/describe.png" />
          <li>Расшифровка</li>
          <img src="@/assets/television.png" />
          <li>Телемедицина</li>
        </div>
      </div>
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
export default {
  name: "my-header",
  components: { MySelect, MyButton },
};
</script>

<style>
li {
  list-style-type: none;
}

.header-container {
  max-width: 1140px;
  padding-left: 30px;
  padding-right: 30px;
  margin: auto;
}

.text-header {
  display: flex;
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
}

.search-input input {
  width: 100%;
  border: none;
  box-sizing: border-box;
  outline: none;
  border-radius: 8px;
  padding-left: 16px;
}

.search-btn {
  border-radius: 0px 8px 8px 0px;
}

.search-icon {
  height: 18px;
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
}

.submenu {
  display: flex;
  flex-direction: row;
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

.submenu-container img {
  margin-right: 6px;
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
</style>
