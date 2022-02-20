<template>
  <div>
    <div class="mainPage">
      <div class="b1">
        <video autoplay playsinline muted loop poster="~/assets/images/sheets/Main/block1/mainBlock1.png">
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
        <p v-if="!mobile" class="bSubTitle b2__bSubTitle">
          {{ datablock2.text }}
        </p>
        <div class="b2__tradingView">
          <tradingView />
        </div>
        <p v-if="mobile" class="bSubTitle b2__bSubTitle">
          {{ datablock2.text }}
        </p>
      </div>
      <div id="block3" class="b3">
        <p class="bTitle b3__bTitle b3__bTitle--upper">
          {{ datablock3.title }}
        </p>
        <p class="bSubTitle b3__bSubTitle b3__bSubTitle--upper" :class="{ 'b3__bSubTitle--toSmallText':mobile}">
          {{ datablock3.text }}
        </p>
        <div class="b3__inner">
          <img
            id="block3_full"
            :src="require('~/assets/images/sheets/Main/block3/full.png')"
            alt=""
            class="b3__img b3__img--full"
          >
          <img
            v-for="image in datablock3.images"
            :key="image.path"
            :src="require(`~/assets/images/sheets/Main/block3/${image.path}`)"
            alt=""
            class="b3__img 'b3__img--anim"
            :class="{
              'b3__img--left': image.cls=='left',
              'b3__img--right': image.cls == 'right'
            }"
          >
        </div>
      </div>
      <div class="b4">
        <div class="b4__col b4__col--back1" :class="{'b4__col--wide':!mobile}">
          <div class="b4__item b4__item--b1">
            <p class="bTitle b4__bTitle b4__bTitle--big">
              {{ datablock4.items[0].title }}
            </p>
            <p class="bBigText b4__bBigText">
              {{ datablock4.items[0].text }}
            </p>
            <svg v-if="mobile" class="b4__svg b4__svg--right" viewBox="0 0 4 262">
              <g filter="url(#filter0_i_379_183)">
                <path d="M4 262L2.29048e-05 262L0 3.49689e-07L3.99998 0L4 262Z" fill="#14161B" />
              </g>
              <defs>
                <filter
                  id="filter0_i_379_183"
                  x="0"
                  y="0"
                  width="4"
                  height="263"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dy="1" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1 0" />
                  <feBlend mode="normal" in2="shape" result="effect1_innerShadow_379_183" />
                </filter>
              </defs>
            </svg>
          </div>
          <div class="b4__item b4__item--b2">
            <p class="bTitle b4__bTitle b4__bTitle--big">
              {{ datablock4.items[1].title }}
            </p>
            <p class="bBigText b4__bBigText">
              {{ datablock4.items[1].text }}
            </p>
            <svg v-if="mobile" class="b4__svg b4__svg--left b4__svg--big " viewBox="0 0 4 305">
              <g filter="url(#filter0_i_379_183)">
                <path d="M4 305L2.66639e-05 305L0 3.49688e-07L3.99997 0L4 305Z" fill="#14161B" />
              </g>
              <defs>
                <filter
                  id="filter0_i_379_183"
                  x="0"
                  y="0"
                  width="4"
                  height="306"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dy="1" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1 0" />
                  <feBlend mode="normal" in2="shape" result="effect1_innerShadow_379_183" />
                </filter>
              </defs>
            </svg>
          </div>
        </div>
        <div class="b4__col--back2" :class="{'b4__col b4__col--middle':!mobile}" />
        <div class="b4__col b4__col--back3" :class="{'b4__col--tall':!mobile}">
          <div class="b4__item b4__item--b3">
            <p class="bTitle b4__bTitle b4__bTitle--big">
              {{ datablock4.items[2].title }}
            </p>
            <p v-for="text in datablock4.items[2].text" :key="text" class="bBigText b4__bBigText">
              {{ text }}
            </p>
          </div>
          <div class="b4__item b4__item--b4">
            <p class="bTitle b4__bTitle b4__bTitle--big">
              {{ datablock4.items[3].title }}
            </p>
            <p v-for="text in datablock4.items[3].text" :key="text" class="bBigText b4__bBigText">
              {{ text }}
            </p>
            <svg v-if="mobile" class="b4__svg b4__svg--right" viewBox="0 0 55 363">
              <g filter="url(#filter0_i_381_273)">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M54.9985 0H50.9985V299.812L0.3125 359.433L3.36005 362.024L54.996 301.5L54.9908 301.497L54.9985 301.5V0Z" fill="#14161B" />
              </g>
              <defs>
                <filter
                  id="filter0_i_381_273"
                  x="0.3125"
                  y="0"
                  width="54.6875"
                  height="363.023"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dy="1" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1 0" />
                  <feBlend mode="normal" in2="shape" result="effect1_innerShadow_381_273" />
                </filter>
              </defs>
            </svg>
          </div>
        </div>
      </div>
      <div id="block5" class="b5" :class="{ 'b5--anim': datablock5.isAfterEnable }">
        <div v-for="item in datablock5.items" :key="item.id" class="b5__item">
          <p class="bTitle b5__bTitle" :class="{'b5__bTitle--fs24':mobile}">
            {{ item.hasOwnProperty('symbol')? item.symbol:'' }}
            {{ item.count | addComma }}
          </p>
          <p class="bSubTitle b5__bSubTitle" :class="{'b5__bSubTitle--fs18':mobile}">
            {{ item.text }}
          </p>
        </div>
      </div>
      <div class="b6">
        <p class="bSmallText b6__bSmallText">
          {{ datablock6.head_text.line1 }}
        </p>
        <p class="bTitle b6__bTitle b6__bTitle--big">
          {{ datablock6.head_text.line2 }}
        </p>
        <joinBlock />
      </div>
    </div>
  </div>
</template>

<script>
// import tradingViewVue from '~/components/tradingView.vue'
export default {
  buildModules: ['nuxt-animejs'],
  name: 'IndexPage',
  filters: {
    addComma (val) {
      return val.toLocaleString()
    }
  },
  components: {
    joinBlock: () => import('~/components/JoinBlock'),
    tradingView: () => import('~/components/tradingView')
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
        isEnabled: false,
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
            title: 'Развитие',
            text: 'Большие обороты холдинг смог набрать после внедрения возможности получения пассивного дохода без необходимости торговать. Любой клиент может выбрать подходящий ему вариант и зарабатывать стабильный доход на проверенных портфелях фонда. Вы сами выбираете сроки инвестирования и риски, на которые вы готовы пойти.'
          },
          {
            id: 3,
            title: 'Детализация',
            text: ['Фонд работает в нескольких направлениях инвестирования:', '-в фармацевтику,', '-в недвижимость, ', ' -в IT-технологии,  ', ' -в криптовалюты,-в онлайн торговлю.  ', ' Для удобства наших клиентов мы предоставляем различые вариации и условия работы с инвестиционными портфелями. Онлайн трейдинг регулируется соотсвенным законодательством регулятора “этой страны.” ']
          },
          {
            id: 4,
            title: 'Продвижение',
            text: ['Для частных инвесторов портфели будут прибыльным инструментом пассивного дохода. Мы ведем прозрачную работу, при которой наши эксперты выбирают самые выгодные варианты инвестирования в различных сферах. За счет того, что холдинг работает с большими объемами - для инвестора снижается риск, ведь его средства инвестируются в сотни или тысячи ценных бумаг или других активов.', 'Для активных трейдеров, мы можем выделить удобство нашего терминала и возможность совмещения счетов с пассивными и активными доходами. Мы получаем котировки напрямую от ведущих европейских банков, что позволяет существенно улучшить качество работы с нашей платформой. ']
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
    // id (value) {
    // },
    // customer: {
    //   deep: true,
    //   handler (obj) {
    //     // console.log(obj)
    //   }
    // }
  },
  created () {
    this.$dark = false
  },
  mounted () {
    window.addEventListener('scroll', this.block5ScrollEvent)
    window.addEventListener('scroll', this.block3ScrollEvent)
  },
  beforeUpdate () {
  },
  beforeDestroy () {
    window.removeEventListener('scroll', this.block5ScrollEvent)
    window.removeEventListener('scroll', this.block3ScrollEvent)
  },
  methods: {
    block3ScrollEvent (event) {
      if (document.querySelector('#block3').getBoundingClientRect().top <= 300 && !this.datablock3.isEnabled && document.querySelector('#block3').getBoundingClientRect().bottom >= 300) {
        this.datablock3.isEnabled = true
        this.$anime({
          targets: ['.b3__img--left', '.b3__img--right'],
          translateX: 0,
          duration: 800,
          easing: 'easeInOutSine'
        })
        this.$anime({
          targets: ['.b3__img--left', '.b3__img--right'],
          opacity: 0,
          delay: 800,
          duration: 800,
          easing: 'easeInOutSine'
        })
        this.$anime({
          targets: '.b3__img--full',
          opacity: 1,
          delay: 800,
          duration: 0,
          easing: 'easeInOutSine'
        })
      }
    },
    block5ScrollEvent (event) {
      if ((document.querySelector('#block5').getBoundingClientRect().top <= 300) && (this.datablock5.isAfterEnable === false)) {
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

.mainPage{
  & .b1{
    margin: vwDesk(30);
    border-radius: vwDesk(40);
    position: relative;
    @media(max-width:$w-adapt){
      margin: 0;
      margin-top: vwMob(48+15);
      padding: 0 vwMob(10) vwMob(15) ;
      border-bottom: 4px solid $clr-border;
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
        right: vwMob(15);
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
      border-bottom: 4px solid $clr-border;
    }
    &__bSubTitle{
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
    }
  }
  & .b3{
    margin-bottom: vwDesk(90);
    position: relative;
    overflow: hidden;
    @media(max-width:$w-adapt){
      margin-top: vwMob(10);
    }
    &__inner{
      background: url(~assets/images/sheets/Main/block3/background.svg);
      background-repeat: no-repeat;
      background-size: contain;
    }
    &__img{
      width:vwDesk(1422);
      margin: 0 auto;
      transition: transform .8s linear;
      @media(max-width:$w-adapt){
        width: vwMob(345);
      }
      &--anim{
        opacity: 1;
        height:vwDesk(150);
      }
      &--left{
        transform: translateX(-20%);
      }
      &--right{
        transform: translateX(20%);
      }
      &--full{
        position: absolute;
        left: 50%;
        bottom: 0%;
        transform: translateX(-50%);
      }
    }

    &__bTitle{
      text-align: center;
      margin-bottom: vwDesk(24);
      @media(max-width:$w-adapt){
        margin-bottom: vwMob(18);
        padding:0 vwMob(25);
      }
      &--upper{
        text-transform: uppercase;
      }
    }
    &__bSubTitle{
      text-align: center;
      margin-bottom:vwDesk(60);
      @media(max-width:$w-adapt){
        padding:0 vwMob(25);
      }
      &--upper{
        text-transform: uppercase;
      }
      &--toSmallText{
        font-size: $fs-12-m;
      }
    }
    & .v-image{
      margin: 0 auto;
    }
  }
  & .b4{
    @include makeitflex(row,flex-start);
    background-size: contain;
    @media(max-width:$w-adapt){
      flex-direction: column;
      border-bottom: 4px solid $clr-border;
    }
    &__svg{
      position: absolute;
      height: 100%;
      top:0;
      &--right{
        right: vwMob(25);
      }
      &--left{
        left: vwMob(15);
      }
      &--big{
        height: 116%;
      }
    }
    &__col{
      @include makeitflex(column,flex-start);
      border-top: 4px $clr-border solid ;
      overflow: hidden;
      background-size:contain;
      &--wide {
        min-width: vwDesk(1125.5);
      border-right: 4px $clr-border solid ;
      }
      &--tall {
        min-width: vwDesk(617);
        border-left: 4px $clr-border solid ;
      }
      &--middle{
        width:100%;
        background-image: url('~/assets/images/sheets/Main/block4/col2.svg');
        border-bottom: 4px $clr-border solid ;
        background-size: cover;
        background-position-y: bottom;
        transition: opacity $anim-time linear !important ;
        position: relative;
        z-index: 1;
        &::after{
          transition: opacity $anim-time linear !important ;
          filter: blur(64px);
          position: absolute;
          left: 0;
          top: 0;
          width: 100%;
          height: 100%;
          z-index: -1;
          content: '';
          opacity: 0;
          background: linear-gradient(175.4deg, rgba(22, 25, 32, 0) 20.47%, #1E232E 55.02%, #22356F 64.22%, #1097BB 79.08%, #00FFE0 95.39%);
          @media(max-width:$w-adapt){
            }
        }
        &:hover::after{
          opacity: 1;
          @media(max-width:$w-adapt){
            opacity:0;
          }
        }
      }
    }
    &__item{
      flex:auto;
      z-index: 1;
      position: relative;
      border-bottom: 4px $clr-border solid ;
      transition: display $anim-time !important ;
      filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
      background-size: contain;

      &--b1{
        background-image: url('~/assets/images/sheets/Main/block4/item1.svg');
        padding: vwDesk(50) vwDesk(120 )vwDesk(90);
        &::after{
          background: linear-gradient(315deg, rgba(22, 25, 32, 0) 62.32%, #1E232E 69.95%, rgba(34, 53, 111, 0.56) 77.2%, rgba(16, 151, 187, 0.61) 88.43%, rgba(0, 255, 224, 0.92) 94.54%, rgba(0, 255, 224, 0.53) 97.75%);
        }
        @media(max-width:$w-adapt){
          // background: linear-gradient(0deg, rgba(22, 25, 32, 0) 62.32%, #1E232E 69.95%, rgba(34, 53, 111, 0.56) 77.2%, rgba(16, 151, 187, 0.61) 88.43%, rgba(0, 255, 224, 0.92) 94.54%, rgba(0, 255, 224, 0.53) 97.75%);
        }
      }
      &--b2{
        padding: vwDesk(50) vwDesk(120 )vwDesk(90);
        background-position-y: bottom;
        background-image: url('~/assets/images/sheets/Main/block4/item2.svg');
        &::after{
          background: linear-gradient(142deg, rgba(22, 25, 32, 0) 54.13%, rgba(30, 35, 46, 0.58) 64.18%, rgba(34, 53, 111, 0.6) 71.44%, rgba(16, 151, 187, 0.68) 80.68%, rgba(11, 182, 198, 0.774518) 83.61%, #00FFE0 90.59%);
          @media(max-width:$w-adapt){
            background: linear-gradient(142deg, rgba(22, 25, 32, 0) 45.44%, #1E232E 65.77%, rgba(34, 53, 111, 0.56) 78.03%, rgba(16, 151, 187, 0.61) 85.7%, rgba(0, 255, 224, 0.92) 95.12%, rgba(0, 255, 224, 0.53) 99.48%);
          }
        }
      }
      &--b3{
        background-image: url('~/assets/images/sheets/Main/block4/item3.svg');
        padding: vwDesk(36) ;
        &::after{
          background: linear-gradient(15deg, rgba(22, 25, 32, 0) 54.43%, #1E232E 71.89%, rgba(34, 53, 111, 0.56) 82.42%, rgba(16, 151, 187, 0.61) 89%, rgba(0, 255, 224, 0.92) 97.09%, rgba(0, 255, 224, 0.53) 101.34%);
          @media(max-width:$w-adapt){
            background: linear-gradient(32deg, rgba(22, 25, 32, 0) 39.09%, rgba(30, 35, 46, 0.58) 56.04%, rgba(34, 53, 111, 0.6) 68.3%, rgba(16, 151, 187, 0.68) 83.9%, #00FFE0 100.62%);
          }
        }
      }
      &--b4{
        background-image: url('~/assets/images/sheets/Main/block4/item4.svg');
        background-position-y: bottom;
        padding: vwDesk(36) ;
        &::after{
          background-image: linear-gradient(204.67deg, rgba(22, 25, 32, 0) 41.66%, #1E232E 59.64%, rgba(34, 53, 111, 0.56) 70.48%, rgba(16, 151, 187, 0.61) 77.26%, rgba(0, 255, 224, 0.92) 85.59%, rgba(0, 255, 224, 0.53) 89.96%);
          @media(max-width:$w-adapt){
            background: linear-gradient(194.28deg, rgba(22, 25, 32, 0) 33.36%, #1E232E 54.49%, rgba(34, 53, 111, 0.56) 67.24%, rgba(16, 151, 187, 0.61) 75.22%, rgba(0, 255, 224, 0.92) 85.02%, rgba(0, 255, 224, 0.53) 90.16%);
          }
        }
      }

      @media(max-width:$w-adapt){
        padding: vwMob(20) vwMob(30);
      }
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
        @media(max-width:$w-adapt){
          opacity:1;
        }
      }
      &:hover::after{
        opacity: 1;
      }
    }
     &__bTitle{
        margin-bottom: $fs-18 ;
        z-index: 10;
        @media(max-width:$w-adapt){
          margin-bottom: $fs-18-m;
        }
        &--big{text-transform: uppercase;}
      }
      &__bBigText{
        z-index: 10;
        &:last-of-type{
          margin-top: $fs-18;
          @media(max-width:$w-adapt){
            margin-top: $fs-14-m;
            padding-right: vwMob(20);
          }
        }
      }
  }
  & .b5{
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
    @media(max-width:$w-adapt){
      @include makeitflex(column, space-between);
      height: vwMob(995);
      padding: vwMob(120) vwMob(85) ;
      margin-bottom: 0;
      background-image: url('~/assets/images/sheets/Main/block5/background_mob.svg');
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

      filter: blur(64px);
      @media(max-width:$w-adapt){
        background:
        linear-gradient(71deg, rgba(22, 25, 32, 0) 50.3%, rgba(30, 35, 46, 0.58) 65.39%, rgba(34, 53, 111, 0.6) 75.76%, rgba(16, 151, 187, 0.68) 85.7%, #00FFE0 95.49%),
        linear-gradient(14deg, rgba(22, 25, 32, 0) 50.83%, rgba(30, 35, 46, 0.58) 65.94%, rgba(34, 53, 111, 0.6) 75.7%, rgba(16, 151, 187, 0.68) 85.85%, #00FFE0 95.8%),
        linear-gradient(322deg, rgba(22, 25, 32, 0) 50.13%, rgba(30, 35, 46, 0.58) 65.57%, rgba(34, 53, 111, 0.6) 75.74%, rgba(16, 151, 187, 0.68) 85.95%, #00FFE0 95.18%);
      //   background: linear-gradient(71deg, rgba(22, 25, 32, 0) 39.3%, rgba(30, 35, 46, 0.58) 55.39%, rgba(34, 53, 111, 0.6) 64.76%, rgba(16, 151, 187, 0.68) 76.7%, #00FFE0 89.49%),
      //   // linear-gradient(4deg, rgba(22, 25, 32, 0) 37.9%, rgba(30, 35, 46, 0.58) 52.31%, rgba(34, 53, 111, 0.6) 62.74%, rgba(16, 151, 187, 0.68) 76.01%, #00FFE0 90.22%),
      // linear-gradient(14deg, rgba(22, 25, 32, 0) 49.83%, rgba(30, 35, 46, 0.58) 61.94%, rgba(34, 53, 111, 0.6) 70.7%, rgba(16, 151, 187, 0.68) 81.85%, #00FFE0 93.8%),
      // linear-gradient(322deg, rgba(22, 25, 32, 0) 34.13%, rgba(30, 35, 46, 0.58) 49.57%, rgba(34, 53, 111, 0.6) 60.74%, rgba(16, 151, 187, 0.68) 74.95%, #00FFE0 90.18%);
      }
    }
     &--anim{
      &::after{
          opacity:1;
      }
    }
    &__item{
      text-align: center;
      flex:1;
      height: fit-content;
      @media(max-width:$w-adapt){
        flex:0;
      }
    }
    &__bTitle{
      &--fs24{
        font-size: $fs-24-m;
      }
    }
    &__bSubTitle{
      max-width: 67%;
      margin: 0 auto;
      @media(max-width:$w-adapt){
        min-width: 100%;
      }
      &--fs18{
        font-size: $fs-18-m;
      }
    }
  }
  & .b6{
    text-align: center;
    // margin-bottom: vwDesk(400);
    &__bSmallText{
      margin-bottom: vwDesk(10);
      text-align: center;
      @media(max-width:$w-adapt){
        margin-bottom: vwMob(15);
        padding: 0 vwMob(25);
      }
    };
    &__bTitle{
      @media(max-width:$w-adapt){
        padding: 0 vwMob(25) vwMob(30);
      }
      &--big{
        font-size: $fs-48;
        @media(max-width:$w-adapt){
          font-size: $fs-18-m;
        }
      }
    };
  }
}
</style>
