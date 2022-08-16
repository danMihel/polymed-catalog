<template>
  <section>
    <h2>{{ subTitle }}</h2>
  </section>
</template>
<script>
export default {
  name: "sub-title",
  props: {
    subTitle: String,
  },
};
</script>
<style scoped>
h2 {
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 500;
  font-size: 32px;
  line-height: 120%;
  color: #1a2a45;
  padding-top: 56px;
  padding-bottom: 40px;
  max-width: 708px;
}
</style>
