<template>
  <SubSubTitle :subsubTitle="label" />
  <div v-for="option in options" :key="option.id">
    <div class="checkbox-items__wraper">
      <div class="checkbox-item"> <label :for="option.id">{{ option }}</label>  <input :id="option.id" type="checkbox" /></div>
    </div>
  </div>
</template>
<script>
import SubSubTitle from "@/components/UI/SubSubTitle.vue";
export default {
  name: "my-checkbox",
  components: {
    SubSubTitle,
},
  props: {
    options: Array,
    label: String,
    default: () => [],
  },
}
  </script>
<style scoped>
.checkbox-item {
  display: flex;
  justify-content: space-between;
  margin-top: 18px;
}
.checkbox-items__wraper {
  width: 87.5%;
}
</style>
