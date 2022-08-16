<template>
  <div class="select-wraper">
    <div @click="show = !show">
      <div class="select-container">
        <div>
          <span class="select-subtitle">Категория анализов</span>
          <div class="select">
            {{ label }}
          </div>
        </div>
        <img v-if="!show" src="@/assets/v.png" />
        <img v-if="show" src="@/assets/up.png" />
      </div>
    </div>
    <transition name="fade">
      <div v-if="show" class="select-items">
        <div v-for="option in options" :key="option.value">
          <div @click="show = !show">{{ option }} 
          
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

.select-wraper {
  margin-top: 32px;
  background: #f7f9fe;
  border: 1px solid #e0e3f4;
  border-radius: 6px;
}
.select-container {
  margin: 9px 9px;
  display: flex;
  justify-content: space-around;
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
  margin-right: 40px;
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
