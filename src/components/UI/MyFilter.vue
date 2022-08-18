<template>
  <section>
    <div class="filter-wraper">
      <div class="filter-str">
        <div>Скидки %</div>
        <div>12</div>
      </div>
      <div class="filter-str">
        <div>Короновирус COVID-19</div>
        <div>23</div>
      </div>
      <div class="filter-str">
        <div>ЗППП</div>
        <div>8</div>
      </div>
      <div class="filter-str active-filter">
        <div>Анализы при беременности</div>
        <div>16</div>
      </div>
      <div class="filter-str">
        <div>Для женщин</div>
        <div>23</div>
      </div>
      <div class="filter-str">
        <div>Для мужчин</div>
        <div>36</div>
      </div>
      <div class="filter-str">
        <div>Для детей</div>
        <div>9</div>
      </div>
      <div class="filter-str">
        <div>Профилактика и госпитализация</div>
        <div>6</div>
      </div>
      <div class="filter-str">
        <div>Спорт и диеты</div>
        <div>12</div>
      </div>
    </div>
  </section>
</template>
<script></script>
<style>
.filter-wraper {
  width: 316px;
  padding-bottom: 32px;
  border-bottom: 1px solid #E0E3F4;
}
.filter-str {
  display: flex;
  justify-content: space-between;
  width: 100%;
  margin-top: 16px;
}
.filter-str div {
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 22px;
}
.active-filter div {
  color: #6d97ff;
}
</style>
