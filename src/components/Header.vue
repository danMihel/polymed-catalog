<template>
  <div>
    <nav class="text-header">
      <li>Пациентам</li>
      <li>Бизнесу</li>
      <li>Франчайзинг</li>
      <li>Интернет магазин</li>
      <Select :options="['О компании']" />
      <Select class="text-header__phone" :options="['8 (800) 33-33-299']" />
      <li>Адреса</li>
      <li>Москва</li>
      <Select :options="['Eng', 'Ru']" />
    </nav>
  </div>
</template>

<script>
import Select from "./UI/Select.vue";
export default {
  name: "header",
  components: { Select },
};
</script>

<style>
li {
  list-style-type: none;
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
  font-family: "PT Root UI" !important;
  font-style: normal !important;
  font-weight: 500 !important;
  font-size: 20px !important;
  line-height: 120% !important;
  color: #ff1b7a !important;
}
</style>
