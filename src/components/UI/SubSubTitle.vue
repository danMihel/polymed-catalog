<template>
  <section>
    <h3>{{ subsubTitle }}</h3>
  </section>
</template>
<script>
export default {
  name: "sub-subtitle",
  props: {
    subsubTitle: String,
  },
};
</script>
<style scoped>
h3 {
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 500;
  font-size: 20px;
  line-height: 120%;
}
</style>
