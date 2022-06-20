<template>
  <nav v-if="isMobileMenuOut">
    <ul>
      <li>Sparkforce</li>
      <li>Cinema App</li>
      <li>Design Tutorial Website</li>
      <li>EduFurther</li>
      <li>Omnix Accounting App</li>
      <li>Eazee Logistic Customer App</li>
      <li>Safetity Trip Planner</li>
      <li>Eazee Logistics Owner App</li>
      <li>Omnix Hotel Management App</li>
      <li>Safetity Wallet</li>
      <li>Eazee Logistics Rider App</li>
      <li>Safetity Places</li>
      <li>Folo</li>
      <li>Safetity Events</li>
      <li>WasteBazaar</li>
      <li>Safetity Marketplace</li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "mobile-menu",
  props: ['isMobileMenuOut']

}
</script>

<style scoped>
nav {
  position: fixed;
  top: 128px;
  width: 100%;
  height: calc(100vh - 128px);
  background: #F2AE0A;
  z-index: 1000;
  padding: 42px;
}
ul {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
}
ul li {
  list-style: none;
  text-decoration: underline;
  cursor: pointer;
  font-size: 18px;
  font-weight: bold;
}

@media screen and (max-width: 650px) {
  nav {
    top: 72px;
    height: calc(100vh - 72px);
  }
}
</style>
