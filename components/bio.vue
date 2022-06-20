<template>
  <section>
    <div class="container bio__inner">
      <p>
        I’m Olawale, i have four (4) years plus of experience in User Experience Design,
        Visual Design, and Interaction Design. I’m passionate about finding the most
        efficient solution to problems in an empathetic way.
      </p>
    </div>
  </section>
</template>

<script>
export default {
  name: "bio"
}
</script>

<style scoped>
section {
  position: relative;
  top: 128px;
  width: 100%;
  background: var(--secondary-color-4);
}
.bio__inner {
  height: 225px;
  font-weight: 400;
  font-size: 22px;
  line-height: 40px;
  display: flex;
  align-items: center;
  color: #000000;
}
.bio__inner p {
  width: 100%;
  max-width: 930px;
}

@media screen and (max-width: 650px) {
  section {
    top: 72px;
  }
  .bio__inner {
    height: auto;
    padding: 34px 0;
  }
  .bio__inner p {
    font-size: 20px;
    line-height: 34px;
  }
}
</style>
