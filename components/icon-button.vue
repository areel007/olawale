<template>
  <button>
    <img v-if="isFigma" src="/assets/images/figma.png" alt="figma">
    <img v-else src="/assets/images/xd-icon.png" alt="xd">
    {{ btnText }}
  </button>
</template>

<script>
export default {
  name: "icon-button",
  props: ['btnText', 'isFigma']
}
</script>

<style scoped>
button {
  border: 1px solid #DBDEE7;
  box-shadow: 0 1px 2px 1px rgba(0, 0, 0, 0.15);
  border-radius: 100px;
  background: white;
  width: 100%;
  padding: 11px 0;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 16px;
}
</style>
