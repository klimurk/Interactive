<template>
  <div>
    <div class="portfolioPage">
      <v-img
        class="pageImgHead"
        :lazy-src="require('~/assets/images/sheets/portfolio/index/head.png')"
        :src="require('~/assets/images/sheets/portfolio/index/head.png')"
        position="center center"
        alt=""
      />
      <p class="bBigTitle portfolioPage__bBigTitle " :class="{'portfolioPage__bBigTitle--fs18':mobile}">
        {{ title }}
      </p>
      <div class="previews">
        <div v-for="portfolio in portfolios" :key="portfolio.name" class="previews__item">
          <v-img
            class="previews__img"
            :src="require(`~/assets/images/sheets/portfolio/index/${portfolio.imgUrl}`)"
          />
          <div class="previews__info">
            <p class="bSubTitle previews__bSubTitle previews__bSubTitle--bold" :class="{'previews__bSubTitle--fs18':mobile}">
              {{ portfolio.name }}
            </p>
            <ul>
              <li v-for="benefit in portfolio.benefits" :key="benefit" class="bSmallText previews__bSmallText" :class="{'previews__bSmallText--fs14':mobile}">
                {{ benefit }}
              </li>
            </ul>
            <a
              class="bSmallText btnBlue previews__btnBlue previews__btnBlue--font"
              @click.prevent="openPage(portfolio.link)"
            >
              {{ portfolio_btn_open }}
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  buildModules: ['nuxt-animejs'],
  name: 'PortfolioPage',
  filters: {},
  components: {
  },
  layout: 'error',
  data () {
    return {
      title: 'Инвестиционные портфели для получения пассивного дохода',
      portfolio_btn_open: 'подробнее',
      portfolios: [
        {
          name: 'Фармацевтика',
          benefits: ['От $100, 000', 'Доходность 7-12%', 'От 1 года'],
          imgUrl: 'preview1.png',
          link: 'pharmaceut'
        },
        {
          name: 'Недвижимость',
          benefits: ['От $150, 000', 'Доходность 9-14%', 'От 2 лет'],
          imgUrl: 'preview2.png',
          link: 'realty'
        },
        {
          name: 'IT технологии',
          benefits: ['От  $200, 000', 'Доходность 11-17%', 'От 3 лет'],
          imgUrl: 'preview3.png',
          link: 'it'
        },
        {
          name: 'Криптовалюты',
          benefits: ['От $300, 000', 'Доходность 19-25%', 'От 2,5 лет'],
          imgUrl: 'preview4.png',
          link: 'crypto'
        }
      ]

    }
  },
  computed: {
    mobile () {
      return this.$vuetify.breakpoint.sm || this.$vuetify.breakpoint.xs
    }
  },
  watch: {},
  created () {},
  mounted () {
  },
  beforeDestroy () {
  },
  methods: {
    // getImgUrl (pic) {
    //   return require('~/assets/images/sheets/portfolio/index/' + pic)
    // },
    openPage (link) {
      this.$router.push('/portfolio/' + link)
    }
  }
}
</script>

<style lang="scss" scoped>
  .portfolioPage{
    &__bBigTitle{
      margin: 0 vwMob(35);
      text-align: center;
      // &--ttc{
      //     text-transform: capitalize;
      // }
      &--fs18{
        font-size: $fs-18-m;
      }
    }
  }
  .previews{
    margin: vwDesk(200) vwDesk(400) ;
    @include makeitflex(row,space-between);
    flex-wrap: wrap;
    @media(max-width:$w-adapt){
      @include makeitflex(column,flex-start);
      margin: 0;
    }
    &__item{
      width: vwDesk(500);
      height: vwDesk(500);
      position: relative;
      margin-bottom: vwDesk(100);
      position: relative;
      z-index: 1;
      &::after{
        content: '';
        position: absolute;
        width: 110%;
        height: 100%;
        left: 50%;
        top: 50%;
        z-index: -1;
        border-radius: 20px;
        transform: translate(-50%,-50%);
        background:
          linear-gradient(178.15deg, rgba(22, 25, 32, 0) -21.98%, rgba(30, 35, 46, 0.58) 12.59%, rgba(34, 53, 111, 0.6) 37.59%, rgba(16, 151, 187, 0.68) 69.41%, #00FFE0 103.5%),
          linear-gradient(178.15deg, rgba(22, 25, 32, 0) -21.98%, rgba(30, 35, 46, 0.406) 12.59%, rgba(34, 53, 111, 0.42) 37.59%, rgba(16, 151, 187, 0.476) 69.41%, rgba(0, 255, 224, 0.7) 103.5%),
          linear-gradient(178.15deg, rgba(22, 25, 32, 0) -21.98%, rgba(30, 35, 46, 0.174) 12.59%, rgba(34, 53, 111, 0.18) 37.59%, rgba(16, 151, 187, 0.204) 69.41%, rgba(0, 255, 224, 0.3) 103.5%);
        filter: blur(40px);
        opacity: 0;
        transition: opacity $anim-time $anim-type;
          // linear-gradient(178.15deg, rgba(22, 25, 32, 0) -21.98%, rgba(30, 35, 46, 0.174) 12.59%, rgba(34, 53, 111, 0.18) 37.59%, rgba(16, 151, 187, 0.204) 69.41%, rgba(0, 255, 224, 0.3) 103.5%);
      }
      &:hover::after{
        opacity:1;
      }
      @media(max-width:$w-adapt){
        width: vwMob(340);
        height: vwMob(340);
        margin: vwMob(25) auto;
      }
    }
    &__img{
      width: 100%;
      height: 100%;
    }
    &__info{
      @include makeitflex(column, space-between);
      position: absolute;
      bottom: 0;
      left: 0;
      height: 215/500*100%;
      width: 100%;
      background: rgba(160, 160, 160, 0.2);
      mix-blend-mode: normal;
      backdrop-filter: blur(40px);

      border-radius: vwDesk(20);
      padding: vwDesk(15) 50% vwDesk(30) vwDesk(20);
      @media(max-width:$w-adapt){
        border-radius: vwMob(20);
        // height: vwMob(150);
        height: auto;
        padding: vwMob(15);
      }
    }
    &__bSubTitle{
      &--bold{
        font-weight: bold !important;
        text-transform: capitalize;
      }
      &--fs18{
        font-size: $fs-18-m;
      }
    }
    &__bSmallText{
      margin: vwDesk(5) 0;
      &--fs14{
        font-size: $fs-14-m;
      }
    }
    &__btnBlue{
      color: $clr-text-1;
      padding: vwDesk(15) vwDesk(40);
      width: fit-content;
      &--font{
        font-weight: bold  !important;
        text-transform: uppercase;
      }
      @media(max-width:$w-adapt){
        padding: vwMob(15) vwMob(35);
        margin-top: vwMob(10);
      }
    }
  }
</style>
