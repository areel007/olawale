<template>
  <section :class="{'is-dark': isNightMode}">
    <div class="container case-studies__inner">

      <div class="case-studies-title">
        <span :class="{'dark-color': isNightMode}">Case Studies</span>
        <div class="line" :class="{'dark-line': isNightMode}"></div>
        <div class="dot" :class="{'dark-dot': isNightMode}"></div>
      </div>

      <div class="mb-5 md:mb-20 case-studies-card__grid">
        <CaseStudiesCard
          v-for="(_card, index) in cards"
          :key="index"
          :card-bg="_card.cardBG"
          :case-study-name="_card.caseStudyName"
          :case-study-details="_card.caseStudyDetails"
          :is-figma="_card.isFigma"
          :is-black="_card.isBlack"
        />
      </div>

    </div>
  </section>
</template>

<script>
import CaseStudiesCard from '../blocks/case-studies-card'
export default {
  name: "case-studies",
  props: ['isNightMode'],
  components: { CaseStudiesCard },
  data () {
    return {
      cards:[
        {
          cardBG: '#FF6500',
          caseStudyName: 'Sparkforce',
          isFigma: true,
          isBlack: true,
          caseStudyDetails: 'A mobile app and website that allow newbies is tech field find job opportunity learning content and inspiring portfolio for career development'
        },
        {
          cardBG: '#F2AE0A',
          caseStudyName: 'Cinema App',
          isFigma: true,
          isBlack: true,
          caseStudyDetails: 'A mobile app that allow users to book movie tickets on their mobile devices'
        },
        {
          cardBG: '#FF7C00',
          caseStudyName: 'Design Tutorials',
          isFigma: false,
          isBlack: true,
          caseStudyDetails: 'A responsive website that allow users to find and view design tutorials'
        },
        {
          cardBG: '#39546D',
          caseStudyName: 'EduFurther',
          isFigma: true,
          isBlack: false,
          caseStudyDetails: 'A progressive web application that allow user to find relevant admission information and mentors that can guide their admission and funding process.'
        },
        {
          cardBG: '#283F54',
          caseStudyName: 'Omnix Accounting App',
          isFigma: true,
          isBlack: false,
          caseStudyDetails: 'A mobile app that allow business owners monitor and manage their business activities and finances on their mobile device'
        },
        {
          cardBG: '#FF6500',
          caseStudyName: 'Eazee Logistics Customer App',
          isFigma: true,
          isBlack: true,
          caseStudyDetails: 'A mobile app that allow users to find logistics company, delivery agent or riders around them in realtime'
        },
        {
          cardBG: '#F2AE0A',
          caseStudyName: 'Safetity Trip Planner',
          isFigma: true,
          isBlack: true,
          caseStudyDetails: 'A progressive web application that allow travelers and tourist easily find travel safety compliance and regulation'
        },
        {
          cardBG: '#FF7C00',
          caseStudyName: 'Eazee Logistics Owner App',
          isFigma: true,
          isBlack: true,
          caseStudyDetails: 'A mobile app that allow logistics company owners to monitor and manage delivery activities of their riders and customers on their mobile devices'
        },
        {
          cardBG: '#39546D',
          caseStudyName: 'Omnix Hotel Management App',
          isFigma: true,
          isBlack: false,
          caseStudyDetails: 'A mobile app that allow hotel owners Monitor and manage their business activities and finances on their mobile device'
        },
        {
          cardBG: '#283F54',
          caseStudyName: 'Safetity Wallet',
          isFigma: true,
          isBlack: false,
          caseStudyDetails: 'A progressive web application that allow users keep their health  and safety document safe and avoiding paper work when needed.'
        },
        {
          cardBG: '#FF6500',
          caseStudyName: 'Eazee Logistics Rider App',
          isFigma: true,
          isBlack: true,
          caseStudyDetails: 'A mobile app that allow logistics company riders to monitor and manage delivery activities assign to them either by customer or company on their mobile devices'
        },
        {
          cardBG: '#F2AE0A',
          caseStudyName: 'Safetity Places',
          isFigma: true,
          isBlack: true,
          caseStudyDetails: 'A progressive web application that allow travelers and tourist easily find places around them and their safety compliance and regulation'
        },
        {
          cardBG: '#FF7C00',
          caseStudyName: 'Folo',
          isFigma: true,
          isBlack: true,
          caseStudyDetails: 'A mobile app that allow users easily find available ride arounf them at realtime'
        },
        {
          cardBG: '#39546D',
          caseStudyName: 'Safetity Events',
          isFigma: true,
          isBlack: false,
          caseStudyDetails: 'A progressive web application that allow event guests easily adhere to events safety compliance and regulation'
        },
        {
          cardBG: '#283F54',
          caseStudyName: 'WasteBazaar',
          isFigma: true,
          isBlack: false,
          caseStudyDetails: 'A mobile app that allow users to easily find waste bus around them to dispose their wastes for hygienic environment'
        },
        {
          cardBG: '#FF6500',
          caseStudyName: 'Safetity Marketplace',
          isFigma: true,
          isBlack: true,
          caseStudyDetails: 'A progressive web application that allow travelers and tourist find and purchase the safety products needed for safe trip'
        },
      ]
    }
  }
}
</script>

<style scoped>
section {
  position: relative;
  top: 128px;
  padding-bottom: 40px !important;
}
.is-dark {
  background: #1E1E1E !important;
}
.case-studies-title {
  padding: 32px 0;
  display: flex;
  align-items: center;
  position: relative;
}
.case-studies-title span {
  font-style: normal;
  font-weight: 700;
  font-size: 22px;
  line-height: 40px;
  color: #283F54;
  white-space: nowrap;
  margin-right: 44px;
}
.dark-color {
  color: #fff !important;
}
.line {
  width: 100%;
  height: 2px;
  background: #283F54;
}
.dark-line {
  background: #fff;
}
.dot {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background: #283F54;
  position: absolute;
  right: 0;
}
.dark-dot {
  background: #fff;
}
.case-studies-card__grid {
  display: grid;
  grid-template-columns: repeat(4, 264px);
  gap: 24px;
}

@media screen and (max-width: 1440px) {
  .case-studies-card__grid {
    grid-template-columns: repeat(3, 1fr);
  }
}
@media screen and (max-width: 900px) {
  .case-studies-card__grid {
    grid-template-columns: repeat(2, 1fr);
  }
}
@media screen and (max-width: 768px) {
  section {
    top: 72px;
  }
}
@media screen and (max-width: 600px) {
  .case-studies-card__grid {
    grid-template-columns: 1fr;
    gap: 5px;
  }
  .case-studies-title {
    padding: 15px 0;
  }
}
</style>
