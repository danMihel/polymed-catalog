<template>
  <select class="select">
    <option v-for="option in options" :key="option.value">
      {{ option }}
    </option>
  </select>
</template>
<script>
export default {
  name: "select",
  props: {
    options: Array,
    default: () => [],
  },
};
</script>
<style>
.select {
  border: none;
  outline: none;
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 120%;
  color: #1a2a45;
}
</style>
