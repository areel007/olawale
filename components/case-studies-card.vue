<template>
<div class="card" :style="cssProps">
  <div class="card__inner">
    <div class="card-front">
      <div class="card-front__bio">
        <img
          :src="isFigma && isBlack?'/assets/images/figma-svg.svg':isFigma && !isBlack?'/assets/images/figma-white.svg':'/assets/images/xd-svg.svg'"
          alt="olawale"
        >
        <span :class="{'is-black': !isBlack}">{{ caseStudyName }}</span>
      </div>
    </div>
    <div class="card-back">
      <h3 :class="{'is-black': !isBlack}">{{ caseStudyName }}</h3>
      <p :class="{'is-black': !isBlack}">{{ caseStudyDetails }}</p>
      <div style="display: flex; flex-direction: column; gap: 12px">
        <PlainButton btn-text="View Case Study" />
        <IconButton btn-text="View Prototype" :is-figma="isFigma" />
      </div>
    </div>
  </div>
</div>
</template>

<script>
import PlainButton from '../../components/blocks/plain-button'
import IconButton from '../../components/blocks/icon-button'

export default {
  name: "case-studies-card",
  props: ['cardBg', 'caseStudyName', 'caseStudyDetails', 'isFigma', 'isBlack'],
  components: { PlainButton, IconButton },
  computed: {
    cssProps () {
      return {
        '--card-bg': this.cardBg,
      }
    }
  }
}
</script>

<style scoped>
.card {
  height: 240px;
  width: 100%;
  background: var(--card-bg);
  cursor: pointer;
}
.card__inner {
  position: relative;
  width: 100%;
  height: 100%;
  /*transition: transform 0.8s;*/
  /*transform-style: preserve-3d;*/
}
.card-front {
  background: var(--card-bg);
}
.card-back {
  height: 320px;
  display: none;
  z-index: 10;
  background: var(--card-bg);
  padding: 30px;
  position: absolute;
}
.card:hover .card-back {
  display: block;
  right: 0;
}

.card-front__bio {
  position: absolute;
  left: 10.61%;
  top: 52.92%;
  bottom: 37.08%;
  display: flex;
  flex-direction: column;
  gap: 16px;
}
.card-front__bio span {
  font-style: normal;
  font-weight: 700;
  font-size: 16px;
  line-height: 24px;
  color: #000;
}
.is-black {
  color: #fff !important;
}
.card-back h3 {
  font-style: normal;
  font-weight: 700;
  font-size: 16px;
  line-height: 24px;
  color: #000000;
}
.card-back p {
  font-style: normal;
  font-weight: 400;
  font-size: 12px;
  line-height: 1.5;
  color: #000000;
  margin-bottom: 10px;
}
.card-front__bio img {
  width: 24px;
}






/*.card:hover .card__inner {*/
/*  transform: rotateY(180deg);*/
/*}*/
/*.card-front, .card-back {*/
/*  position: absolute;*/
/*  width: 100%;*/
/*  height: 100%;*/
/*  -webkit-backface-visibility: hidden;*/
/*  backface-visibility: hidden;*/
/*}*/
/*.card-front {*/
/*  color: black;*/
/*  display: flex;*/
/*  flex-direction: column;*/
/*  gap: 16px;*/
/*}*/
/*.card-back {*/
/*  padding: 30px;*/
/*  transform: rotateY(180deg);*/
/*  display: flex;*/
/*  flex-direction: column;*/
/*  justify-content: space-between;*/
/*}*/
</style>
