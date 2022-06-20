<template>
  <div class="floating">
    <a href="">
      <img src="/assets/images/dribbble.png" alt="dribbble">
    </a>
    <a href="">
      <img src="/assets/images/behance.png" alt="dribbble">
    </a>
    <a href="">
      <img src="/assets/images/linkedin.png" alt="dribbble">
    </a>
    <a href="">
      <img src="/assets/images/twitter.png" alt="dribbble">
    </a>
    <a href="">
      <img src="/assets/images/gmail.png" alt="dribbble">
    </a>
  </div>
</template>

<script>
export default {
  name: "floating"
}
</script>

<style scoped>
.floating {
  padding: 31px 16px;
  background: white;
  position: fixed;
  top: 233px;
  right: 21%;
  z-index: 100;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  gap: 32px;
  box-shadow: 0 1px 2px 1px rgba(0, 0, 0, 0.15);
  border-radius: 100px;
}
.floating a {
  display: flex;
  align-items: center;
}

@media screen and (max-width: 1440px) {
  .floating {
    right: 12%;
  }
}

@media screen and (max-width: 768px) {
  .floating {
    padding: 16px 31px;
    flex-direction: row;
    top: 84vh;
    right: 50%;
    transform: translateX(50%);
  }
}

@media screen and (max-width: 500px) {
  .floating {
    gap: 10px;
  }
}
</style>
