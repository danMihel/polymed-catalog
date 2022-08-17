<template>
  <section>
    <form>
      <div class="subscribe-wraper">
        <div class="subscribe-col">
          <div class="subscribe-title">Подпишитесь и будьте в курсе</div>
          <div>
            Получайте специальные предложение и актуальные
            <br />скидки на наши услуги продукты
          </div>
        </div>
        <div class="subscribe-col">
          <div>
            <input
              class="subscribe-input"
              type="email"
              placeholder="Введите свой E-mail"
            />
            <MyButton :title="'Подписаться'" />
          </div>

          <br />
          <input
            type="checkbox"
            class="custom-checkbox"
            id="subscribe"
            name="subscribe"
            value="1"
          />
          <label for="subscribe">
            <div>
              Принимаю условия &nbsp; <a>оферты</a> и &nbsp;<a>политики</a>
              <br />
              <a>конфиденциальности</a>
            </div>
          </label>
        </div>
      </div>
    </form>
  </section>
</template>
<script>
import SubTitle from "@/components/UI/SubTitle.vue";
import MyButton from "@/components/UI/MyButton.vue";
export default {
  name: "subscrube-form",
  components: { SubTitle, MyButton },
};
</script>
<style scoped>
a {
  font-weight: 600;
}
.subscribe-wraper {
  display: flex;
  justify-content: space-around;
  background: #6d97ff;
  color: #ffffff;
  height: 216px;
  margin-top: 112px;
}
.subscribe-col {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.subscribe-title {
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 500;
  font-size: 32px;
  line-height: 120%;
  margin-bottom: 16px;
}
.subscribe-input {
  border: none;
  box-sizing: border-box;
  outline: none;
  padding-left: 24px;
  width: 401px;
  height: 44px;
  margin-right: 16px;
  border-radius: 6px;
}
.custom-checkbox {
  position: absolute;
  z-index: -1;
  opacity: 0;
}
.custom-checkbox + label {
  display: inline-flex;
  align-items: center;
  user-select: none;
}
.custom-checkbox + label::before {
  content: "";
  display: inline-block;
  width: 18px;
  height: 18px;
  flex-shrink: 0;
  flex-grow: 0;
  border: 2px solid #ffffff;
  border-radius: 4px;
  margin-right: 8px;
  background-repeat: no-repeat;
  background-position: center center;
  background-size: 50% 50%;
}

.custom-checkbox:checked + label::before {
  border-color: #0b76ef;
  background-color: #0b76ef;
  background-image: url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 8 8'%3e%3cpath fill='%23fff' d='M6.564.75l-3.59 3.612-1.538-1.55L0 4.26 2.974 7.25 8 2.193z'/%3e%3c/svg%3e");
}
</style>
