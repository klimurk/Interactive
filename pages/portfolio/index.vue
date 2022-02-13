<template>
  <div>
    <div class="portfolioPage">
      <v-img
        class="pageImgHead"
        :lazy-src="require('~/assets/images/sheets/portfolio/index/head.png')"
        :src="require('~/assets/images/sheets/portfolio/index/head.png')"
        width="96%"
        alt=""
      />
      <p>
        {{ title }}
      </p>
      <div class="portfolioPage_previews">
        <div v-for="portfolio in portfolios" :key="portfolio.name" class="portfolioPage_previews_item">
          <v-img
            class="item_img"
            :lazy-src="getImgUrl(portfolio.imgUrl)"
            :src="getImgUrl(portfolio.imgUrl)"
          />
          <div class="item_info">
            <p class="title">
              {{ portfolio.name }}
            </p>
            <ul>
              <li v-for="benefit in portfolio.benefits" :key="benefit">
                {{ benefit }}
              </li>
            </ul>
            <a
              class="item_btn btn_blue"
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
    // joinblock: () => import('~/components/joinBlock')
  },
  layout: 'error',
  data () {
    return {
      title: 'Инвестиционные портфели для получения пассивного дохода',
      portfolio_btn_open: 'подробнее',
      portfolios: [
        {
          name: 'ФАРМАЦЕ́ВТИКА',
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
  computed: {},
  watch: {},
  created () {},
  mounted () {
    // window.addEventListener('scroll', this.block1ScrollEvent)
  },
  beforeDestroy () {
    // window.removeEventListener('scroll', this.block1ScrollEvent)
  },
  methods: {
    getImgUrl (pic) {
      return require('~/assets/images/sheets/portfolio/index/' + pic)
    },
    openPage (link) {
      this.$router.push('/portfolio/' + link)
    }
  }
}
</script>

<style lang="scss" scoped>
  .portfolioPage{
    &>p{
      font-family: 'Manrope', sans-serif !important;
      font-style: normal !important;
      font-weight: 800 !important;
      font-size: $h2FS !important;
      line-height: 1;
      /* or 48px */

      text-align: center;
      letter-spacing: 0.05em;
      text-transform: capitalize;
    }
    &_previews{
      margin: 200/1920*100vw 400/1920*100vw ;
      @include makeitflex(row,space-between);
      flex-wrap: wrap;
      &_item{
        width: 500/1920*100vw;
        height: 500/1920*100vw;
        position: relative;
        margin-bottom: 100/1920*100vw;
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
          transition: opacity $transition_time $transition_anim_type;
            // linear-gradient(178.15deg, rgba(22, 25, 32, 0) -21.98%, rgba(30, 35, 46, 0.174) 12.59%, rgba(34, 53, 111, 0.18) 37.59%, rgba(16, 151, 187, 0.204) 69.41%, rgba(0, 255, 224, 0.3) 103.5%);
        }
        // &::before{
        //   background: linear-gradient(178.15deg, rgba(22, 25, 32, 0) -21.98%, rgba(30, 35, 46, 0.174) 12.59%, rgba(34, 53, 111, 0.18) 37.59%, rgba(16, 151, 187, 0.204) 69.41%, rgba(0, 255, 224, 0.3) 103.5%);
        //   filter: blur(70px);
        // }
        &:hover::after{
          opacity:1;
        }
        & .item{
          &_img{
            width: 100%;
            height: 100%;
          }
          &_info{
            @include makeitflex(column, space-between);
            position: absolute;
            bottom: 0;
            left: 0;
            height: 215/500*100%;
            width: 100%;
            background: rgba(160, 160, 160, 0.2);
            mix-blend-mode: normal;
            backdrop-filter: blur(40px);
            /* Note: backdrop-filter has minimal browser support */

            border-radius: 20px;
            padding: 15/1920*100vw 50% 30/1920*100vw 20/1920*100vw;
            font-family: 'Manrope', sans-serif !important;
            font-style: normal;
            & .title{
              font-weight: bold !important;
              font-size: $h5FS;
              line-height: 1;
            }
            &>ul>li{
              font-weight: normal;
              font-size: $h7FS;
              line-height: 24/14*1;
            }
            & .item_btn{
              color: $textColor1;
              padding: 15/1920*100vw 40/1920*100vw;
              width: fit-content;
              font-family: 'Roboto', sans-serif !important;
              font-style: normal !important;
              font-weight: bold  !important;
              font-size: $h7FS  !important;
              letter-spacing: 0.05em;
              text-transform: uppercase;
            }
          }
        }
      }
    }
  }
</style>
