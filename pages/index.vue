<template>
  <div>
    <div class="mainPage">
      <div class="mainPage_block1">
        <video autoplay playsinline muted loop poster="~/assets/images/temp/mainBlock1.png">
          <source src="~/assets/video/main/block1.mp4" type="video/mp4">
        </video>
        <div class="mainPage_block1_description">
          <p class="title">
            {{ datablock1.title }}
          </p>
          <br>
          <p>
            {{ datablock1.text }}
          </p>
          <br>
          <a href="">
            {{ datablock1.btn_text }}
          </a>
        </div>
      </div>
      <div class="mainPage_block2">
        <div>
          <p class="title">
            {{ datablock1.title }}
          </p>
          <p class="text">
            {{ datablock1.text }}
          </p>
        </div>
        <v-img lazy-src="/assets/images/temp/mainBlock2.png" :src="require('~/assets/images/temp/mainBlock2.png')" alt="" />
      </div>
      <div id="block3" class="mainPage_block3">
        <p class="title">
          {{ datablock3.title }}
        </p>
        <p class="text">
          {{ datablock3.text }}
        </p>
        <v-img
          id="block3_full"
          lazy-src="/assets/images/pages/Main/block3/full.png"
          :src="require('/assets/images/pages/Main/block3/full.png')"
          width="74vw"
          alt=""
          class="full"
        />
        <v-img
          v-for="image in datablock3.images"
          :key="image.path"
          :lazy-src="`/assets/images/pages/Main/block3/${image.path}`"
          :src="require(`/assets/images/pages/Main/block3/${image.path}` )"
          aspect-ratio="12.365"
          width="74vw"
          height="0,05989vw"
          alt=""
          :class="{
            left: image.cls=='left',
            right: image.cls == 'right'
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
.mainPage{
  &_block1{
    padding: 30px;
    border-radius: 40px;
    position: relative;
    &>video{
      width: 100%;
      border-radius: 40px;
    }
    &_description{
      position: absolute;
      right: 137/1840*100%;
      top: 400/1022*100%;
      max-width: 666/1840*100%;
      font-size: $h6FS !important;
      .title{
        font-family: 'Manrope', sans-serif  !important;
        font-size: $h4FS !important;
        line-height: 1.25;
      }
      >a{
        color: $textColor1;
        transition: color $transition_time $transition_anim_type;
        &:hover{
            color: $btncolor1;
        }
      }
    }
  }
  &_block2{
    padding: 30px 70px;
    .text{
      text-align: center;
      font-family: 'Raleway', sans-serif;
      margin: 0 auto 48/1920*100vw;

      max-width: 1620/1920*100vw;
    }
    .title{
      max-width: 1620/1920*100vw;
      text-align: center;
      font-family: 'Manrope', sans-serif  !important;
      margin: 0 auto 48/1920*100vw;
      font-size: $h4FS  !important;
      font-weight: 800;
      line-height: 1;
      letter-spacing: 0.05em  !important;
    }

  }
  &_block3{
    margin-bottom: 90px;
    position: relative;
    & .left{
      transform: translateX(-20%);
      transition: transform .8s linear;
    }
    & .right{
      transform: translateX(20%);
      transition: transform .8s linear;
    }
    & .full{
      display: none;
      position: absolute;
      left: 50%;
      bottom: 0%;
      transform: translateX(-50%);
    }
    & .title{
      font-family: 'Manrope', sans-serif  !important;
      font-size: $h4FS !important;
      line-height: 1.5;
      font-weight: 800;
      letter-spacing: 0.05em !important;
      text-align: center;
    }
    & .text{
      font-size: $h5FS !important;
      font-weight: 600;
      line-height: 1.5;
      letter-spacing: 0.05em !important;
      text-align: center;
      margin-bottom: 60px;
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
      transition: display $transition_time !important ;
      filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
      &::after{
        opacity: 0;
        transition: opacity $transition_time linear !important ;
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
        font-size: $h4FS !important;
        margin-bottom: $h6FS !important;
        z-index: 10;
      }
      & .text{
        font-family: 'Manrope', sans-serif  !important;
        font-weight: 300 !important;
        font-size: $h6FS !important;
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
      min-width:1125.5/1920*100%;
      border-right: 4px #14161B solid ;
      background-image: url('~/assets/images/pages/Main/block4/col1.svg');
      & .mainPage_block4_item{
        padding: 50px 118px;
      }
    }
    .tall {
      min-width: 617/1920*100%;
      border-left: 4px #14161B solid ;
      background-image: url('~/assets/images/pages/Main/block4/col3.svg');
      & .mainPage_block4_item{
        padding: 40px 30px;
      }
    }
    .middle{
      width:100%;
      border-bottom: 4px #14161B solid ;
      background-image: url('~/assets/images/pages/Main/block4/col2.svg');
      background-size: cover;
      background-position-y: bottom;
    }
  }
  &_block5{
    @include makeitflex(row, space-between);
    background-image: url('~/assets/images/pages/Main/block5/background.svg');
    background-size: contain;
    height: 584px;
    width: 100%;
    margin-bottom: 80px;
    padding: 307px 200px 0;
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
      transition: opacity $transition_time linear !important ;
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
        font-size: $h1FS !important ;
        line-height: 87/64*1 !important;
        font-feature-settings: 'pnum' on, 'lnum' on;
      }
      .text{
        font-weight: 500 !important;
        font-size: $h5FS !important;
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
      font-size: $h7FS !important;
      margin-bottom: 10px;
    };
    & .title{
      font-family: 'Manrope', sans-serif  !important;
      font-weight: 800 !important;
      font-size: $h2FS !important;
    };
  }
}
//  @import url('~/assets/scss/pages/mainPage/_block1.scss');
  // @import url('~/assets/scss/pages/mainPage/_main.scss');
</style>
