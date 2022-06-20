<template>
  <header :class="{'is-dark': isNightMode}">
    <div class="container header__inner">
      <img :src="isNightMode?'/assets/images/logo-dark.svg':'/assets/images/logo-light.svg'" alt="olawale" class="logo">
      <div class="header-option-btn">
        <button class="download-resume">
          <span>Download Resume</span>
          <img src="/assets/images/download.png" alt="download resume">
        </button>
        <button class="mode-switch" @click="$emit('toggle-mode')">
          <img src="/assets/images/mode-switch.png" alt="mode switch">
        </button>
        <button class="menu-btn" @click="$emit('toggle-mobile-menu')">
          <img v-if="!isMobileMenuOut" src="/assets/images/hamburger.png" alt="olawale">
          <img v-else src="/assets/images/close.svg" alt="olawale">
        </button>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "app-header",
  props: ['isNightMode', 'isMobileMenuOut']
}
</script>

<style scoped>
header {
  position: fixed;
  width: 100%;
  background: white;
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.15);
  z-index: 100;
}
.is-dark {
  background: #1A1C1E !important;
}
.header__inner {
  height: 128px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.header-option-btn {
  display: flex;
  align-items: center;
}
.download-resume {
  height: 72px;
  padding: 24px 34px;
  border-radius: 100px;
  box-shadow: 0 1px 2px 1px rgba(0, 0, 0, 0.15);
  display: flex;
  align-items: center;
  margin-right: 24px;
  background: #fff;
}
.download-resume span {
  margin-right: 16px;
}
.mode-switch {
  height: 72px;
  width: 72px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  margin-right: 24px;
  box-shadow: 0 1px 2px 1px rgba(0, 0, 0, 0.15);
  background: #fff;
}
.menu-btn {
  height: 72px;
  width: 72px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  box-shadow: 0 1px 2px 1px rgba(0, 0, 0, 0.15);
  background: #fff;
}
.download-resume span {
  font-size: 16px;
  color: var(--primary-color-4);
}

@media screen and (max-width: 768px) {
  .download-resume span {
    display: none;
  }
}
@media screen and (max-width: 650px) {
  .header__inner {
    height: 72px;
  }
  .logo {
    width: 105px;
  }
  .header__inner button img {
    width: 18px;
  }
  .download-resume,
  .mode-switch {
    width: 56px;
    height: 56px;
    padding: 0;
    border-radius: 50%;
    justify-content: center;
    margin-right: 16px;
  }
  .menu-btn {
    width: 56px;
    height: 56px;
    padding: 0;
    border-radius: 50%;
    justify-content: center;
  }
}
</style>
