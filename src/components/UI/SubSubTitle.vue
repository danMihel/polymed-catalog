<template>
  <section>
    <div class="h3">{{ subsubTitle }}</div>
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
.h3 {
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 500;
  font-size: 20px;
  line-height: 120%;
  margin-top: 32px;
  margin-bottom: 32px;
}
</style>
