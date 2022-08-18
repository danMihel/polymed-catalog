<template>
  <div class="search-input">
    <input
      class=" "
      type="search"
      placeholder="Быстрый поиск нужного исследования..."
    />
    <img class="search-btn" src="@/assets/Search-icon.png" />
  </div>
</template>
<script>
export default {
  name: "search-input",
};
</script>
<style scoped>

.search-input {
  
  border: 1px solid #ff1b7a;
  max-width: 600px;
  height: 44px;
  border-radius: 8px;
  margin-right: 7px;
}

.search-input input {
  width: 100%;
  border: none;
  box-sizing: border-box;
  outline: none;
  border-radius: 8px;
  padding-left: 16px;
}

.search-btn {
  border-radius: 0px 8px 8px 0px;
}

.search-icon {
  height: 18px;
}

</style>
