<template>
  <section>
    <div class="card-container">
      <div class="card-left">
        <div class="card-index">{{ product.index }}</div>
        <div class="card-text">{{ product.text }}</div>
        <div class="card-left__base">
          <img src="@/assets/clock.png" />
          <div>{{ product.terms }}</div>
          <img src="@/assets/house.png" />
           <div>{{ product.home }}</div>
        </div>
      </div>
      <div class="card-right">
        <div class="card-prise">{{ product.prise }}</div>
        <div class="card-blood">Вен. кровь (+180₽)</div>
        <MyButton class="card-btn" :title="'В корзину'" />
      </div>
    </div>
  </section>
</template>
<script>
import MyButton from "./UI/MyButton.vue";
export default {
  name: "my-product",
  props: {
    product: {
      type: Object,
      require: true,
    },
  },
  components: { MyButton },
};
</script>
<style>
.card-container {
  display: flex;
  padding: 32px;
  background: #f7f9fe;
  border: 1px solid #e6e6e6;
  border-radius: 16px;
  max-width: 752px;
  margin-top: 24px;
}
.card-left {
  display: flex;
  align-items: flex-start;
  flex-direction: column;
  max-width: 532px;
  margin-right: 25px;
}
.card-right {
  width: 70%;
  align-items: flex-end;
  display: flex;
  flex-direction: column;
}

.card-btn {
  margin-top: 16px;
  width: 132px;
  height: 44px;
}

.card-index {
  background: #e0e3f4;
  border-radius: 4px;
  padding: 6px 12px;
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 700;
  font-size: 12px;
  line-height: 12px;
  color: #8790ae;
}

.card-text {
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 500;
  font-size: 18px;
  line-height: 26px;
  color: #1a2a45;
  margin-top: 22px;
}

.card-prise {
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 700;
  font-size: 24px;
  line-height: 30px;
  color: #1a2a45;
}

.card-blood {
  margin-top: 4px;
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 400;
  font-size: 12px;
  line-height: 16px;
  color: #8790ae;
}

.card-left__base {
  display: flex;
  align-items: center;
  margin-top: 18px;
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 400;
  font-size: 12px;
  line-height: 16px;
  color: #8790AE;
}

.card-left__base img{
  margin-right: 10px;
}

.card-left__base div{
  margin-right: 24px;
}
</style>
