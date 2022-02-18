<template>
  <div>
    <div class="mainPage">
      <div class="b1">
        <video autoplay playsinline muted loop poster="~/assets/images/temp/mainBlock1.png">
          <source src="~/assets/video/main/block1.mp4" type="video/mp4">
        </video>
        <div class="bTitle b1__bTitle b1__text--pos">
          {{ datablock1.title }}
        </div>
        <div
          class="bBigText b1__bBigText"
          :class="{ 'b1__text--pos': !mobile }"
        >
          <p>
            {{ datablock1.text }}
          </p>
          <br>
          <a class="link" href="">
            {{ datablock1.btn_text }}
          </a>
        </div>
      </div>
      <div class="b2">
        <p class="bTitle b2__bTitle">
          {{ datablock2.title }}
        </p>
        <p v-if="!mobile" class="bSubtitle b2__bSubtitle">
          {{ datablock2.text }}
        </p>
        <div class="b2__tradingView">
          <!-- TradingView Widget BEGIN -->
          <div class="tradingview-widget-container">
            <div class="tradingview-widget-container__widget" />
            <div class="tradingview-widget-copyright">
              <a href="https://www.tradingview.com/markets/" rel="noopener" target="_blank"><span class="blue-text">Financial Markets</span></a> by TradingView
            </div>
            <script type="text/javascript" src="https://s3.tradingview.com/external-embedding/embed-widget-market-overview.js" async>
              {
              "colorTheme": "dark",
              "dateRange": "12M",
              "showChart": true,
              "locale": "en",
              "width": "100%",
              "height": "100%",
              "largeChartUrl": "",
              "isTransparent": false,
              "showSymbolLogo": true,
              "showFloatingTooltip": false,
              "plotLineColorGrowing": "rgba(41, 98, 255, 1)",
              "plotLineColorFalling": "rgba(41, 98, 255, 1)",
              "gridLineColor": "rgba(240, 243, 250, 0)",
              "scaleFontColor": "rgba(120, 123, 134, 1)",
              "belowLineFillColorGrowing": "rgba(41, 98, 255, 0.12)",
              "belowLineFillColorFalling": "rgba(41, 98, 255, 0.12)",
              "belowLineFillColorGrowingBottom": "rgba(41, 98, 255, 0)",
              "belowLineFillColorFallingBottom": "rgba(41, 98, 255, 0)",
              "symbolActiveColor": "rgba(41, 98, 255, 0.12)",
              "tabs": [
              {
              "title": "Indices",
              "symbols": [
              {
              "s": "FOREXCOM:SPXUSD",
              "d": "S&P 500"
              },
              {
              "s": "FOREXCOM:NSXUSD",
              "d": "US 100"
              },
              {
              "s": "FOREXCOM:DJI",
              "d": "Dow 30"
              },
              {
              "s": "INDEX:NKY",
              "d": "Nikkei 225"
              },
              {
              "s": "INDEX:DEU40",
              "d": "DAX Index"
              },
              {
              "s": "FOREXCOM:UKXGBP",
              "d": "UK 100"
              }
              ],
              "originalTitle": "Indices"
              },
              {
              "title": "Futures",
              "symbols": [
              {
              "s": "CME_MINI:ES1!",
              "d": "S&P 500"
              },
              {
              "s": "CME:6E1!",
              "d": "Euro"
              },
              {
              "s": "COMEX:GC1!",
              "d": "Gold"
              },
              {
              "s": "NYMEX:CL1!",
              "d": "Crude Oil"
              },
              {
              "s": "NYMEX:NG1!",
              "d": "Natural Gas"
              },
              {
              "s": "CBOT:ZC1!",
              "d": "Corn"
              }
              ],
              "originalTitle": "Futures"
              },
              {
              "title": "Bonds",
              "symbols": [
              {
              "s": "CME:GE1!",
              "d": "Eurodollar"
              },
              {
              "s": "CBOT:ZB1!",
              "d": "T-Bond"
              },
              {
              "s": "CBOT:UB1!",
              "d": "Ultra T-Bond"
              },
              {
              "s": "EUREX:FGBL1!",
              "d": "Euro Bund"
              },
              {
              "s": "EUREX:FBTP1!",
              "d": "Euro BTP"
              },
              {
              "s": "EUREX:FGBM1!",
              "d": "Euro BOBL"
              }
              ],
              "originalTitle": "Bonds"
              },
              {
              "title": "Forex",
              "symbols": [
              {
              "s": "FX:EURUSD"
              },
              {
              "s": "FX:GBPUSD"
              },
              {
              "s": "FX:USDJPY"
              },
              {
              "s": "FX:USDCHF"
              },
              {
              "s": "FX:AUDUSD"
              },
              {
              "s": "FX:USDCAD"
              }
              ],
              "originalTitle": "Forex"
              }
              ]
              }
            </script>
          </div>
          <!-- TradingView Widget END -->
        </div>
        <p v-if="mobile" class="bSubtitle b2__bSubtitle">
          {{ datablock2.text }}
        </p>
      </div>
      <div id="block3" class="b3">
        <p class="bTitle b3__bTitle b3__bTitle--upper">
          {{ datablock3.title }}
        </p>
        <p class="bSubtitle b3__bSubtitle b3__bSubtitle--upper">
          {{ datablock3.text }}
        </p>
        <v-img
          id="block3_full"
          lazy-src="/assets/images/sheets/Main/block3/full.png"
          :src="require('/assets/images/sheets/Main/block3/full.png')"
          alt=""
          class="b3__img b3__img--full"
        />
        <v-img
          v-for="image in datablock3.images"
          :key="image.path"
          :lazy-src="`/assets/images/sheets/Main/block3/${image.path}`"
          :src="require(`/assets/images/sheets/Main/block3/${image.path}` )"
          aspect-ratio="12.365"
          width="74vw"
          height="0,05989vw"
          alt=""
          class="b3__img"
          :class="{
            'b3__img--left': image.cls=='left',
            'b3__img--right': image.cls == 'right'
          }"
        />
      </div>
      <div class="mainPage_block4">
        <div class="mainPage_block4_col wide">
          <div class="mainPage_block4_item datablock4_b1">
            <p class="title">
              {{ datablock4.items[0].title }}
            </p>
            <p class="text">
              {{ datablock4.items[0].text }}
            </p>
          </div>
          <div class="mainPage_block4_item datablock4_b2">
            <p class="title">
              {{ datablock4.items[1].title }}
            </p>
            <p class="text">
              {{ datablock4.items[1].text }}
            </p>
          </div>
        </div>
        <div class="mainPage_block4_col middle" />
        <div class="mainPage_block4_col tall">
          <div class="mainPage_block4_item datablock4_b3">
            <p class="title">
              {{ datablock4.items[2].title }}
            </p>
            <p class="text">
              {{ datablock4.items[2].text }}
            </p>
          </div>
          <div class="mainPage_block4_item datablock4_b4">
            <p class="title">
              {{ datablock4.items[3].title }}
            </p>
            <p class="text">
              {{ datablock4.items[3].text }}
            </p>
          </div>
        </div>
      </div>
      <div
        id="block5"
        class="mainPage_block5"
        :class="{ afterEnable: datablock5.isAfterEnable }"
      >
        <div v-for="item in datablock5.items" :key="item.id" class="mainPage_block5_item">
          <p class="title">
            {{ item.hasOwnProperty('symbol')? item.symbol:'' }}
            {{ item.count | addComma }}
          </p>
          <p class="text">
            {{ item.text }}
          </p>
        </div>
      </div>
      <div class="mainPage_block6">
        <p class="text">
          {{ datablock6.head_text.line1 }}
        </p>
        <p class="title textTitle">
          {{ datablock6.head_text.line2 }}
        </p>
        <joinblock />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  buildModules: ['nuxt-animejs'],
  name: 'IndexPage',
  filters: {
    addComma (val) {
      return val.toLocaleString()
    }
  },
  components: {
    joinblock: () => import('~/components/joinBlock')
  },
  layout: 'error',
  data () {
    return {
      datablock1:
      {
        title: 'Различные инвестиционные портфели: Недвижимость Фармацевтика,  IT-технологии',
        text: 'Определите вашу инвестиционную цель и инвестируйте без рисков.Простой способ долгосрочного инвестирования в готовые решения от нашего фонда.',
        btn_text: 'Читать дальше'
      },
      datablock2:
      {
        title: 'Мгновенный доступ ко всем вариантам заработка на мировых финансовых рынках',
        text: 'Вместе с нами вы сможете инвестировать в IT-технологии, недвижимость и крупнейшие мировые компании. А также торговать криптовалютами, покупать/продавать сырьевые товары или спекулировать различными валютами и активами.'
      },
      datablock3:
      {
        title: 'Инновационные решения для инвестирования и торговли',
        text: 'Получайте пассивный доход или занимайтесь активной торговлей - выбор за вами.',
        images:
        [
          {
            path: 'part1.png',
            cls: 'right'
          },
          {
            path: 'part2.png',
            cls: 'left'
          },
          {
            path: 'part3.png',
            cls: 'right'
          },
          {
            path: 'part4.png',
            cls: 'left'
          },
          {
            path: 'part5.png',
            cls: 'right'
          },
          {
            path: 'part6.png',
            cls: 'left'
          }
        ]
      },
      datablock4:
      {
        items: [
          {
            id: 1,
            title: 'Начало',
            text: 'История фонда берет свое начало с того момента, когда трейдеры и экономисты решили создать свою финансовую экосистему, которая даст возможность зарабатывать простым людям. Целью этого проекта было развитие и внедрение систем комплексного инвестирования для упрощения работы с инвестициями и торговли на финансовых рынках.'
          },
          {
            id: 2,
            title: 'Детализация',
            text: 'Фонд работает в нескольких направлениях инвестирования: /r -в фармацевтику, /r -в недвижимость, /r -в IT-технологии, /r -в криптовалюты,-в онлайн торговлю. /r  /r Для удобства наших клиентов мы предоставляем различые вариации и условия работы с инвестиционными портфелями. Онлайн трейдинг регулируется соотсвенным законодательством регулятора “этой страны.” '
          },
          {
            id: 3,
            title: 'Развитие',
            text: 'Большие обороты холдинг смог набрать после внедрения возможности получения пассивного дохода без необходимости торговать. Любой клиент может выбрать подходящий ему вариант и зарабатывать стабильный доход на проверенных портфелях фонда. Вы сами выбираете сроки инвестирования и риски, на которые вы готовы пойти.'
          },
          {
            id: 4,
            title: 'Продвижение',
            text: 'Для частных инвесторов портфели будут прибыльным инструментом пассивного дохода. Мы ведем прозрачную работу, при которой наши эксперты выбирают самые выгодные варианты инвестирования в различных сферах. За счет того, что холдинг работает с большими объемами - для инвестора снижается риск, ведь его средства инвестируются в сотни или тысячи ценных бумаг или других активов.  /r  /r Для активных трейдеров, мы можем выделить удобство нашего терминала и возможность совмещения счетов с пассивными и активными доходами. Мы получаем котировки напрямую от ведущих европейских банков, что позволяет существенно улучшить качество работы с нашей платформой. '
          }
        ]
      },
      datablock5:
      {
        isAfterEnable: false,
        items: [
          {
            id: 0,
            value: 3754,
            count: 0,
            text: 'подписанных контрактов за последний месяц'
          },
          {
            id: 1,
            symbol: '$',
            value: 13681062,
            count: 0,
            text: 'объем выходящих транзакций'
          },
          {
            id: 2,
            value: 17780641,
            count: 0,
            text: 'заключено сделок на платформе'
          }
        ]
      },
      datablock6:
      {
        head_text:
        {
          line1: 'InteractiveFund не взимает никаких дополнительных комисcий на ввод/вывод средств.',
          line2: 'Пополняйте и выводите без ограничений'
        }
      }
    }
  },
  computed: {
    mobile () {
      return this.$vuetify.breakpoint.sm || this.$vuetify.breakpoint.xs
    }
  },
  watch: {
    id (value) {
    },
    customer: {
      deep: true,
      handler (obj) {
        // console.log(obj)
      }
    }
  },
  created () {
    this.$dark = false
  },
  mounted () {
    window.addEventListener('scroll', this.block5ScrollEvent)
    window.addEventListener('scroll', this.block3ScrollEvent)
  },
  beforeUpdate () {
    document.getElementsByClassName('tv-embed-widget-wrapper__body')[0].style.border = '0'
  },
  beforeDestroy () {
    window.removeEventListener('scroll', this.block5ScrollEvent)
    window.removeEventListener('scroll', this.block3ScrollEvent)
  },
  methods: {
    block3ScrollEvent (event) {
      if (document.querySelector('#block3').getBoundingClientRect().top <= 300) {
        this.$anime({
          targets: ['.left', '.right'],
          translateX: '0',
          duration: 800,
          easing: 'easeInOutSine'
        })
        this.$anime({
          targets: ['.left', '.right'],
          opacity: '0',
          delay: 800,
          duration: 800,
          easing: 'easeInOutSine'
        })
        setTimeout(() => {
          document.getElementById('block3_full').style.display = 'block'
        }, 800)
      }
    },
    block5ScrollEvent (event) {
      if ((document.querySelector('#block5').getBoundingClientRect().top <= 300) && (this.datablock5.items[0].count === 0)) {
        this.datablock5.isAfterEnable = true
        this.datablock5.items.forEach((item) => {
          const obj = { n: item.count }
          this.$anime({
            targets: obj,
            n: item.value,
            round: 1,
            duration: 700,
            easing: 'easeInOutSine',
            update: () => {
              item.count = obj.n
            }
          })
        })
      }
    }
  }
}
</script>

<style scoped lang="scss">

// @import url('~/assets/scss/abstracts/_variables.scss');
.bTitle{
  font-size: $fs-36;
  line-height: 1.25;
  font-weight: 800;
  @media(max-width:$w-adapt){
    font-size: $fs-18-m;
  }
}
.bSubTitle{

  font-size: $fs-24;
  font-weight: 500;
  line-height: 32/24*1;
  font-family: Manrope;
  font-style: normal;
  letter-spacing: 5%;
  @media(max-width:$w-adapt){
    font-size: $fs-14-m;
  }

}
.link{
  color: $clr-text-1;
  transition: color $anim-time $anim-type;
  &:hover{
      color: $clr-btn-1;
  }
}
.bBigText{
  font-size: $fs-18;
  font-weight: normal;
  @media(max-width:$w-adapt){
    font-size: $fs-14-m;
  }
}
.mainPage{
  & .b1{
    margin: vwDesk(30);
    border-radius: vwDesk(40);
    position: relative;
    @media(max-width:$w-adapt){
      margin: vwMob(48+15) vwMob(10) vwMob(15) ;
    }
    &>video{
      width: 100%;
      border-radius: vwDesk(40);
    }
    &__text--pos{
      position: absolute;
      right: vwDesk(47);
      max-width: vwDesk(885);
      @media(max-width:$w-adapt){
        rigth: vwMob(15);
        max-width: vwMob(158)
      }
    }
    &__bTitle{
      top: vwDesk(400);
      @media(max-width:$w-adapt){
        top: vwMob(35);
      }
    }
    &__bBigText{
      top: vwDesk(550);

      @media(max-width:$w-adapt){
        top: 0;
        max-width: 100%;
        padding: vwMob(20) vwMob(14);

      }
    }
  }
  & .b2{
    padding: vwDesk(30) vwDesk(70);
    @media(max-width:$w-adapt){
      padding:vwMob(8) vwMob(25) vwMob(13);
    }
    &__bSubtitle{
      text-align: center;
      margin: 0 auto vwDesk(48);
      max-width: vwDesk(1620);
      @media(max-width:$w-adapt){
        margin:0;
        text-align:left;
      }
    }
    &__bTitle{
      max-width: vwDesk(1620);
      text-align: center;
      margin: 0 auto vwDesk(48);
      @media(max-width:$w-adapt){
        max-width: 100%;
      }
    }
    &__tradingView{
      height: vwDesk(912);
      border-radius: vwDesk(40);
      overflow: hidden;
      border: 2px solid #434651;
      @media(max-width:$w-adapt){
        margin-bottom: vwMob(15);
        height: vwMob(190);
      }
      & .tradingview-widget-container{
          & .tv-embed-widget-wrapper {
            width: 60px !important;
            height: auto;
          }
          .tv-embed-widget-wrapper__body{
            border: 0;
        }
      }
    }
  }
  & .b3{
    margin-bottom: vwDesk(90);
    position: relative;
    overflow: hidden;
    &__img{
      width:vwDesk(1422);
      &--left{
        transform: translateX(-20%);
        transition: transform .8s linear;
      }
      &--right{
        transform: translateX(20%);
        transition: transform .8s linear;
      }
      &--full{
        display: none;
        position: absolute;
        left: 50%;
        bottom: 0%;
        transform: translateX(-50%);
      }
    }

    &__bTitle{
      text-align: center;
      @media(max-width:$w-adapt){
        margin-bottom: vwMob(18);
      }
      &--upper{
        text-transform: uppercase;
      }
    }
    &__bSubtitle{
      text-align: center;
      margin-bottom:vwDesk(60);
      &--upper{
        text-transform: uppercase;
      }
    }
    & .v-image{
      margin: 0 auto;
    }
  }
  &_block4{
    @include makeitflex(row,flex-start);
    background-size: contain;
    &_col{
      @include makeitflex(column,flex-start);
      border-top: 4px #14161B solid ;
      overflow: hidden;
      background-size:contain;
    }
    &_item{
      flex:auto;
      z-index: 1;
      position: relative;
      border-bottom: 4px #14161B solid ;
      transition: display $anim-time !important ;
      filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
      &::after{
        opacity: 0;
        transition: opacity $anim-time linear !important ;
        filter: blur(64px);
        position: absolute;
        left: 0;
        top: 0;
        width: 100%;
        height: 100%;
        z-index: -1;
        content: '';
      }
      &:hover::after{
        opacity: 1;
      }
      & .title{
        font-family: 'Manrope', sans-serif  !important;
        font-weight: 600 !important;
        font-size: $fs-36 !important;
        margin-bottom: $fs-18 !important;
        z-index: 10;
      }
      & .text{
        font-family: 'Manrope', sans-serif  !important;
        font-weight: 300 !important;
        font-size: $fs-18 !important;
        z-index: 10;
      }
    }

    .datablock4{
      &_b1::after{
        background: linear-gradient(315deg, rgba(22, 25, 32, 0) 62.32%, #1E232E 69.95%, rgba(34, 53, 111, 0.56) 77.2%, rgba(16, 151, 187, 0.61) 88.43%, rgba(0, 255, 224, 0.92) 94.54%, rgba(0, 255, 224, 0.53) 97.75%);
      }
      &_b2::after{
        background: linear-gradient(142deg, rgba(22, 25, 32, 0) 54.13%, rgba(30, 35, 46, 0.58) 64.18%, rgba(34, 53, 111, 0.6) 71.44%, rgba(16, 151, 187, 0.68) 80.68%, rgba(11, 182, 198, 0.774518) 83.61%, #00FFE0 90.59%);
      }
      &_b3::after{
        background: linear-gradient(15deg, rgba(22, 25, 32, 0) 54.43%, #1E232E 71.89%, rgba(34, 53, 111, 0.56) 82.42%, rgba(16, 151, 187, 0.61) 89%, rgba(0, 255, 224, 0.92) 97.09%, rgba(0, 255, 224, 0.53) 101.34%);
      }
      &_b4::after{
        background-image: linear-gradient(204.67deg, rgba(22, 25, 32, 0) 41.66%, #1E232E 59.64%, rgba(34, 53, 111, 0.56) 70.48%, rgba(16, 151, 187, 0.61) 77.26%, rgba(0, 255, 224, 0.92) 85.59%, rgba(0, 255, 224, 0.53) 89.96%);
      }
    }
    .wide {
      min-width: vwDesk(1125.5);
      border-right: 4px #14161B solid ;
      background-image: url('~/assets/images/sheets/Main/block4/col1.svg');
      & .mainPage_block4_item{
        padding: 50px 118px;
      }
    }
    .tall {
      min-width: vwDesk(617);
      border-left: 4px #14161B solid ;
      background-image: url('~/assets/images/sheets/Main/block4/col3.svg');
      & .mainPage_block4_item{
        padding: 40px 30px;
      }
    }
    .middle{
      width:100%;
      border-bottom: 4px #14161B solid ;
      background-image: url('~/assets/images/sheets/Main/block4/col2.svg');
      background-size: cover;
      background-position-y: bottom;
    }
  }
  &_block5{
    @include makeitflex(row, space-between);
    background-image: url('~/assets/images/sheets/Main/block5/background.svg');
    background-size: contain;
    height: vwDesk(584);
    width: 100%;
    margin-bottom: vwDesk(80);
    padding: vwDesk(307) vwDesk(200) 0;
    position: relative;
    z-index: 1;
    overflow: hidden;
    &.afterEnable{
      &::after{
          opacity:1;
      }
    }
    &::after{
      opacity: 0;
      transition: opacity $anim-time linear !important ;
      position: absolute;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      z-index: -1;
      content: '';
      background: linear-gradient(4deg, rgba(22, 25, 32, 0) 37.9%, rgba(30, 35, 46, 0.58) 52.31%, rgba(34, 53, 111, 0.6) 62.74%, rgba(16, 151, 187, 0.68) 76.01%, #00FFE0 90.22%);
      filter: blur(64px);
    }
    &_item{
      text-align: center;
      flex:1;
      height: fit-content;
      .title{
        font-family: 'Manrope', sans-serif  !important;
        font-weight: bold !important;
        font-size: $fs-64 !important ;
        line-height: 87/64*1 !important;
        font-feature-settings: 'pnum' on, 'lnum' on;
      }
      .text{
        font-weight: 500 !important;
        font-size: $fs-24 !important;
        line-height: 33/24*1 !important;
        font-feature-settings: 'pnum' on, 'lnum' on;
        max-width: 67%;
        margin: 0 auto;
      }
    }
  }
  &_block6{
    text-align: center;
    // margin-bottom: 400px;
    & .text{
      font-family: 'Manrope', sans-serif  !important;
      font-weight: 500 !important;
      font-size: $fs-14 !important;
      margin-bottom: 10px;
    };
    & .title{
      font-family: 'Manrope', sans-serif  !important;
      font-weight: 800 !important;
      font-size: $fs-48 !important;
    };
  }
}
//  @import url('~/assets/scss/sheets/mainPage/_block1.scss');
  // @import url('~/assets/scss/sheets/mainPage/_main.scss');
</style>
