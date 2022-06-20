<template>
  <footer :class="{'dark-footer': isNightMode}">
    <div class="container footer__inner">
      <img :src="isNightMode?'/assets/images/logo-dark.svg':'/assets/images/logo-light.svg'" alt="olawale">
      <span :class="{'dark-color': isNightMode}">&copy; Copyright Olawale 2022</span>
    </div>
  </footer>
</template>

<script>
export default {
  name: "app-footer",
  props: ['isNightMode']
}
</script>

<style scoped>
footer {
  position: relative;
  top: 128px;
  box-shadow: 0px 1px 2px 1px rgba(0, 0, 0, 0.15);
}
.dark-footer {
  background: #1A1C1E !important;
}
.footer__inner {
  height: 120px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.dark-color {
  color: #fff;
}

@media screen and (max-width: 650px) {
  footer {
    top: 72px;
  }
  .footer__inner {
    height: 70px;
  }
}
</style>
