<template>
  <section>
    <h2>{{ text }}</h2>
  </section>
</template>
<script>
export default {
  name: "my-title",
  props: {
    text: String,
  },
};
</script>
<style scoped>
h2 {
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 500;
  font-size: 44px;
  line-height: 56px;
  color: #1a2a45;
  padding-top: 24px;
  padding-bottom: 24px;
  border-bottom: 1px solid #e0e3f4;
  max-width: 708px;
}
@media (max-width: 810px) {
  h2 {
    font-size: 30px;
    line-height: 36px;
  }
}
</style>
