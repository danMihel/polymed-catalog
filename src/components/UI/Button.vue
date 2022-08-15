<template>
    <button class="button">
        {{ title }}
    </button>
</template>
<script>
export default {
    name: "button",
    props: {
        title: String,
    },
};
</script>
<style>
.button {
    width: 141px;
    height: 44px;
    left: 1149px;
    top: 72px;
    background: #FF1B7A;
    border-radius: 8px;
    border: none;
    color: #FFFFFF;
    font-family: 'PT Root UI';
    font-style: normal;
    font-weight: 500;
    font-size: 18px;
    line-height: 26px;
}
</style>
