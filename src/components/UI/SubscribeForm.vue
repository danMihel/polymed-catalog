<template>
  <section>
    <div class="subscribe-wraper">
      <div>
        <SubTitle :subTitle="'Подпишитесь и будьте в курсе'" />
      </div>
      <div></div>
    </div>
  </section>
</template>
<script>
import SubTitle from "./SubTitle.vue";
export default {
  name: "subscrube-form",
  components: { SubTitle },
};
</script>
<style scoped>
.subscribe-wraper{
    display: flex;
    justify-content: center;
    border: 1px solid red;
}
</style>
