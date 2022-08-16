<template>
  <MyHeader />
  <div class="container">
    <MyTitle :text="'Анализы при беременности'" />
    <SubTitle :subTitle="'Планирование беременности'" />
    <div class="analis-wraper">
      <div class="analis-left">
        <div
          class="product"
          v-for="item of $store.state.pregnancy"
          :key="item.id"
        >
          <Product
            :product="item"
            :key="Date.now()"
            class="product-container"
          />
        </div>
        <SubTitle :subTitle="'Обследования во время беременности'" />
      </div>
      <div class="analis-right">
        <SubSubTitle :subsubTitle="'Быстрый фильтр'"/>
        <MyFilter/>
        <FilterSelect :label="'Анализы при беременности'" :options="['Скидки %', 'Короновирус COVID-19', 'Профилактика и госпитализация']" />
        <ChekboxSelect :options="['Муж', 'Жен']" :label="'Ваш пол'"/>
        <ChekboxSelect :options="['Здоровый', 'Не очень']" :label="'Какой образ жизни'"/>
        <ChekboxSelect :options="['Насморк', 'Температура']" :label="'Симптомы'"/>
        <ChekboxSelect :options="['Если бы мы знали, что это такое', 'Мы не занем, что это такое']" :label="'Нозологии'"/>  
      </div>
    </div>
  </div>
</template>

<script>
import MyHeader from "@/components/MyHeader.vue";
import MyTitle from "@/components/UI/MyTitle.vue";
import SubTitle from "./components/UI/SubTitle.vue";
import Product from "./components/Product.vue";
import SubSubTitle from "./components/UI/SubSubTitle.vue";
import MyFilter from "./components/UI/MyFilter.vue";
import FilterSelect from "./components/UI/FilterSelect.vue";
import ChekboxSelect from "./components/UI/ChekboxSelect.vue";

export default {
  name: "App",
  components: {
    MyHeader,
    MyTitle,
    SubTitle,
    Product,
    SubSubTitle,
    MyFilter,
    FilterSelect,
    ChekboxSelect
},
};
</script>

<style>
#app {
  margin-top: 22px;
}

.container {
  max-width: 1140px;
  padding-left: 30px;
  padding-right: 30px;
  margin: auto;
}
.analis-wraper{
display: flex;
}
.analis-left {
  margin-right: 48px;
  
}
.analis-right {
  
  
}
</style>
