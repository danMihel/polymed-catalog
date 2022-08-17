<template>
  <section>
    <div class="basement-container">
      <div class="basement-wraper">
        <div>
          <img class="logo" src="@/assets/logo.png" />
        </div>
        <div class="bord">
          <a href="https://www.whatsapp.com/">
            <div class="assistent-wraper">
              <img src="@/assets/whats.png" />
              <span class="assistent-wraper-text">
                Помощник Полимед в WhatsApp
              </span>
            </div>
          </a>
          <a href="https://telegram.me/">
            <div class="assistent-wraper">
              <img src="@/assets/telegram.png" />
              <span class="assistent-wraper-text">
                Помощник Полимед в Telegram
              </span>
            </div>
          </a>
        </div>
        <div>
          <img src="@/assets/visa.png" />
        </div>
      </div>
      <div class="basement-wraper">
        <div class="basement-text">© 2022 ООО «Полимед»</div>
        <div class="basement-text">
          Продолжая использовать наш сайт, вы даете согласие на обработку файлов
          <a>Cookies</a> и других пользовательских данных, в соответствии с
          <a>Политикой конфиденциальности</a> и
          <a>Пользовательским соглашением</a>
        </div>
        <div class="basement-social">
          <img src="@/assets/twitter.png" />
          <img src="@/assets/youtube.png" />
          <img src="@/assets/vk.png" />
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: "basement",
};
</script>
<style>
a {
  text-decoration: none;
}
.basement-container {
  margin-top: 43px;
  margin-bottom: 56px;
}
.bord { 
 width: 380px;
}
.basement-wraper {
  flex-wrap: wrap;
  display: flex;
  justify-content: space-around;
  margin-bottom: 44px;
}
.basement-col {
  display: flex;
  flex-direction: column;
}
.logo {
  width: 170px;
  height: 42px;
  margin-right: 16px;
}
.basement-copy {
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 400;
  font-size: 15px;
  line-height: 120%;
  color: #8790ae;
}
.assistent-wraper {
  display: flex;
  align-items: center;
  margin-bottom: 22px;
}

.assistent-wraper-text {
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 400;
  font-size: 15px;
  line-height: 120%;
  color: #1a2a45;
  margin-left: 16px;
}

.basement-text {
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 400;
  font-size: 15px;
  line-height: 120%;
  color: #8790ae;
  max-width: 400px;
}

.basement-text a {
  color: rgb(31, 189, 255);
}
.basement-social {
  display: flex;
  align-items: center;
}
.basement-social img {
  margin-left: 32px;
}
</style>
