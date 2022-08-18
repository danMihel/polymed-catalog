<template>
  <div class="select-wraper">
    <div @click="show = !show">
      <div class="select-container">
        <label class="select">
          {{ label }}
        </label>
        <div class="select-right">
          <div class="select-sum">1</div>
          <img v-if="!show" src="@/assets/v.png" />
          <img v-if="show" src="@/assets/up.png" />
        </div>
      </div>
    </div>
    <transition name="fade">
      <div v-if="show" class="select-items">
        <div v-for="option in options" :key="option.value">
          <div class="select-items__wraper">
            <div class="select-item">
              {{ option }} <input type="checkbox" />
            </div>
          </div>
        </div>
      </div>
    </transition>
  </div>
</template>
<script>
export default {
  name: "my-select",
  props: {
    options: Array,
    label: String,
    default: () => [],
  },
    
  data() {
    return {
      show: false,
    };
  },
};
</script>
<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.2s ease-out;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
.select-item {
  display: flex;
  justify-content: space-between;
  margin-top: 18px;
}
.select-items__wraper {
  width: 87.5%;
}
.select-right {
  display: flex;
}
.select-sum {
  width: 30px;
  height: 30px;
  background: rgba(109, 151, 255, 0.7);
  border-radius: 4px;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #ffffff;
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 500;
  font-size: 15px;
  line-height: 22px;
  margin-right: 14px;
}
.select-wraper {
  margin-top: 32px;
  background: #f7f9fe;
  border: 1px solid #e0e3f4;
  border-radius: 6px;
}
.select-container {
  margin: 18px 16px;
  display: flex;
  justify-content: space-between;
}
.select-container img {
  align-self: flex-end;
  margin-top: auto;
  margin-bottom: auto;
  margin-right: 24px;
}
.select {
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 22px;
  color: #1a2a45;
  align-self: center;
}
.select-items {
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 22px;
  color: #1a2a45;
  margin-left: 19px;
  margin-bottom: 9px;
}
.select-subtitle {
  font-family: "PT Root UI";
  font-style: normal;
  font-weight: 400;
  font-size: 12px;
  line-height: 16px;
  color: #8790ae;
}
</style>
