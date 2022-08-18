<template>
  <section>
    <div class="contacts-wraper">
      <div class="contacts-col phone">
        <div class="contacts-phone-wraper">
          <a class="contacts-phone" href="8 (800) 33-33-299">
            8 (800) 33-33-299</a
          >
          <div class="contacts-phone-sub">Бесплатный звонок по России</div>
        </div>
        <div class="contacts-phone-wraper">
          <a class="contacts-phone" href="+7 (495) 150-80-32">
            +7 (495) 150-80-32</a
          >
          <div class="contacts-phone-sub">Бесплатный звонок по России</div>
        </div>
        <div class="contacts-btn">
          <img src="@/assets/phone.png" />Позвоните мне
        </div>
      </div>
      <div class="contacts-col ">
        <p><a>Пациентам</a></p>
        <p><a>Корпоративным &nbsp;клиентам</a></p>
        <p><a>Франчайзинг</a></p>
        <p><a>Вакцинация</a></p>
        <p><a>Интернет-магазин</a></p>
      </div>
      <div class="contacts-col">
        <p><a>Пресс-центр</a></p>
        <p><a>О компании</a></p>
        <p><a>Партнёры</a></p>
        <p><a>Работа в компании</a></p>
        <p><a>Юридическая информация</a></p>
        <p><a>Контакты</a></p>
      </div>
      <div class="contacts-col">
        <p><a>Лабораторные услуги</a></p>
        <p><a>Запись к врачу</a></p>
        <p><a>Выезд на дом</a></p>
        <p><a>Адреса медцентров</a></p>
        <p><a>Расшифровка анализов</a></p>
        <p><a>Телемедецина</a></p>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: "contacts",
};
</script>
<style scoped>
.contacts-wraper {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  margin-top: 57px;
  padding-bottom: 49px;
  border-bottom: 1px solid #e0e3f4;
  padding-right: 10px;
  padding-left: 10px;
}
.contacts-col {
  margin-right: 5px;
}
.contacts-col p {
  margin-bottom: 16px;
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 400;
  font-size: 15px;
  line-height: 120%;
  color: #1a2a45;
}
.contacts-btn {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 206px;
  height: 44px;
  background: #ff1b7a;
  border-radius: 8px;
  color: #ffffff;
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 500;
  font-size: 18px;
  line-height: 26px;
  margin-top: 24px;
}
.contacts-btn img {
  margin-right: 13px;
  height: 14px;
  width: 14px;
}
.contacts-phone {
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 400;
  font-size: 32px;
  line-height: 120%;
  color: #1a2a45;
  text-decoration: none;
}
.contacts-phone-sub {
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 400;
  font-size: 15px;
  line-height: 120%;
  color: #8790ae;
}
.contacts-phone-wraper {
  margin-bottom: 39px;
}
@media (max-width: 810px) {
  .phone {
    display: flex;
    flex-direction: column;
    align-items: center;
    flex-wrap: wrap;
    margin-bottom: 60px;
    width: 100%;
  }
  .contacts-phone {
    margin-right: 10px;
  }
}
@media (max-width: 530px) {
  .contacts-col{
    width: 100%;
    text-align: center;
  }
}
</style>
