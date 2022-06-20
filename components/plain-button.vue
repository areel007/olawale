<template>
  <button>{{ btnText }}</button>
</template>

<script>
export default {
  name: "plain-button",
  props: ['btnText']
}
</script>

<style scoped>
button {
  border: 1px solid #DBDEE7;
  box-shadow: 0 1px 2px 1px rgba(0, 0, 0, 0.15);
  border-radius: 100px;
  background: #283F54;
  width: 100%;
  padding: 11px 0;
  color: #fff;
}
</style>
