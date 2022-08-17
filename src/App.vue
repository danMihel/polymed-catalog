<template>
  <MyHeader />
  <section>
    <div class="container">
      <MyTitle :text="'Анализы при беременности'" />
      <SubTitle class="subtitle" :subTitle="'Планирование беременности'" />
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
          <SubTitle
            class="subtitle"
            :subTitle="'Обследования во время беременности'"
          />
          <div
            class="product"
            v-for="item of $store.state.survey"
            :key="item.id"
          >
            <Product
              :product="item"
              :key="Date.now()"
              class="product-container"
            />
          </div>
          <div class="next-btn__wraper">
            <MyButton class="next-btn" :title="'Показать еще'" />
          </div>
        </div>
        <div>
          <SubSubTitle class="subtitle" :subsubTitle="'Быстрый фильтр'" />
          <MyFilter />
          <FilterSelect
            :label="'Анализы при беременности'"
            :options="[
              'Скидки %',
              'Короновирус COVID-19',
              'Профилактика и госпитализация',
            ]"
          />
          <ChekboxSelect :options="['Муж', 'Жен']" :label="'Ваш пол'" />
          <ChekboxSelect
            :options="['Здоровый', 'Не очень']"
            :label="'Какой образ жизни'"
          />
          <ChekboxSelect
            :options="['Насморк', 'Температура']"
            :label="'Симптомы'"
          />
          <ChekboxSelect
            :options="[
              'Если бы мы знали, что это такое',
              'Мы не занем, что это такое',
            ]"
            :label="'Нозологии'"
          />
          <div class="trash-container">
            <div class="trash">
              <img src="@/assets/trash.png" />
              <p>Сбросить все фильтры</p>
            </div>
          </div>
          <div class="chekbox-wraper">
            <MyChekbox
              :options="[
                'I триместр',
                'II триместр',
                'III триместр',
                'Осложнения беременность',
              ]"
              :label="'Беременность'"
            />
          </div>
          <div class="chekbox-wraper">
            <MyChekbox
              :options="[
                'Хламидиоз',
                'Сифилис',
                'ВИЧ',
                'Гонорея',
                'Герпес',
                'Папилломавирус',
                'Уреа- и микоплазмоз',
                'Трихомониаз',
                'Кандидоз',
              ]"
              :label="'ЗППП'"
            />
          </div>
          <div class="chekbox-wraper">
            <MyChekbox :options="['Мониторинг беременности']" />
          </div>
          <div class="chekbox-wraper">
            <MyChekbox :options="['Общий анализ крови']" />
          </div>
          <MyChekbox :options="['Общий анализ мочи']" />
        </div>
      </div>
    </div>
  </section>
  <SubscribeForm />
  <Contacts/>
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
import MyChekbox from "./components/UI/MyChekbox.vue";
import MyButton from "./components/UI/MyButton.vue";
import SubscribeForm from "@/components/SubscribeForm.vue";
import Contacts from "./components/Contacts.vue";

export default {
  name: "App",
  components: {
    SubscribeForm,
    MyButton,
    MyHeader,
    MyTitle,
    SubTitle,
    Product,
    SubSubTitle,
    MyFilter,
    FilterSelect,
    ChekboxSelect,
    MyChekbox,
    MyButton,
    Contacts
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
.analis-wraper {
  display: flex;
}
.analis-left {
  margin-right: 48px;
}
.subtitle {
  margin-top: 80px;
  margin-bottom: 40px;
}

.trash-container {
  display: flex;
  padding: 34px;
  border-bottom: 1px solid #e0e3f4;
}

.trash {
  display: flex;
  align-items: center;
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 22px;
  color: #00b4ff;
  margin: auto;
}

.trash img {
  margin-right: 12px;
}
.chekbox-wraper {
  border-bottom: 1px solid #e0e3f4;
  padding-bottom: 33px;
}

.next-btn {
  width: 162px !important;
  height: 44px !important;
  background-color: #ffffff;
  border: 1px solid #ff1b7a;
  color: #ff1b7a;
}

.next-btn__wraper {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 48px;
}
</style>
