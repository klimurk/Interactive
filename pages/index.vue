<template>
  <div>
    <div class="mainPage">
      <div class="mainPage_block1">
        <v-img
          lazy-src="/assets/images/temp/mainBlock1.png"
          :src="require('~/assets/images/temp/mainBlock1.png')"
          alt=""
        />
        <div class="mainPage_block1_description">
          <p class="title">
            Различные инвестиционные портфели: Недвижимость Фармацевтика,  IT-технологии
          </p>
          <br>
          <p>
            Определите вашу инвестиционную цель и инвестируйте без рисков.Простой способ долгосрочного инвестирования в готовые решения от нашего фонда.
          </p>
          <br>
          <a href="">
            Читать дальше
          </a>
        </div>
      </div>
      <div class="mainPage_block2">
        <div>
          <p class="title">
            Мгновенный доступ ко всем вариантам заработка на мировых финансовых рынках
          </p>
          <p class="text">
            Вместе с нами вы сможете инвестировать в IT-технологии, недвижимость и крупнейшие мировые компании. А также торговать криптовалютами, покупать/продавать сырьевые товары или спекулировать различными валютами и активами.
          </p>
        </div>
        <v-img lazy-src="/assets/images/temp/mainBlock2.png" :src="require('~/assets/images/temp/mainBlock2.png')" alt="" />
      </div>
      <div class="mainPage_block3">
        <div class="mainPage_block3_col wide">
          <div class="mainPage_block3_item dataBlock3_b1">
            <p class="title">
              {{ datablock3_items[0].title }}
            </p>
            <p class="text">
              {{ datablock3_items[0].text }}
            </p>
          </div>
          <div class="mainPage_block3_item dataBlock3_b2">
            <p class="title">
              {{ datablock3_items[1].title }}
            </p>
            <p class="text">
              {{ datablock3_items[1].text }}
            </p>
          </div>
        </div>
        <div class="mainPage_block3_col middle"></div>
        <div class="mainPage_block3_col tall">
          <div class="mainPage_block3_item dataBlock3_b3">
            <p class="title">
              {{ datablock3_items[2].title }}
            </p>
            <p class="text">
              {{ datablock3_items[2].text }}
            </p>
          </div>
          <div class="mainPage_block3_item dataBlock3_b4">
            <p class="title">
              {{ datablock3_items[3].title }}
            </p>
            <p class="text">
              {{ datablock3_items[3].text }}
            </p>
          </div>
        </div>
        <!-- <div
          v-for="item in datablock3_items"
          :key="item.id"
          class="mainPage_block3_item"
          :class="{ dataBlock3_b1: item.id == 1,
                    dataBlock3_b2: item.id == 2,
                    dataBlock3_b3: item.id == 3,
                    dataBlock3_b4: item.id == 4,
                    wide: item.id % 2 == 1,
                    tall: item.id % 2 == 0}"
        >
          <p class="title">
            {{ item.title }}
          </p>
          <p class="text">
            {{ item.text }}
          </p>
        </div> -->
      </div>
      <!-- <form-card title="nazvanie" :id.sync="id" @submit="func"></form-card> -->
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  layout: 'error',
  // components: {
  //   formCard: () => import('~/components/card')
  // },
  data () {
    return {
      id: 0,
      customer: {
        id: 25,
        text: 'sdsdsd'
      },
      datablock3_items: [
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
    }
  },
  computed: {

  },
  watch: {
    id (value) {
      console.log(value)
    },
    customer: {
      deep: true,
      handler (obj) {
        console.log(obj)
      }
    }
  },
  created () {
    console.log('created')
    this.$dark = false
  },
  mounted () {
    console.log('mounted')
  },
  methods: {

  }
}
</script>

<style scoped lang="scss">

@import url('~/assets/scss/abstracts/_placeholders.scss');
@import url('~/assets/scss/abstracts/_variables.scss');
.mainPage{
  &_block1{
    padding: 30px;
    border-radius: 40px;
    position: relative;
    &_description{
      position: absolute;
      right: 137/1840*100%;
      top: 400/1022*100%;
      max-width: 666/1840*100%;
        font-size: $h6FS !important;
      .title{
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
      font-family: 'Manrope', sans-serif;
      margin: 0 auto 48/1920*100vw;
      font-size: $h4FS;
      font-weight: 800;
      line-height: 1;
      letter-spacing: 0.05em;
    }

  }
  &_block3{
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
        &::after{
          // opacity: 0;
          display: none;
          transition: all $transition_time !important ;
        }
      filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
      &:hover{
        &::after{
          display: block;
          // opacity:1;
          filter: blur(64px);
          position: absolute;
          left: 0;
          top: 0;
          width: 100%;
          height: 100%;
          z-index: -1;
          content: '';
        }
      }
      & .title{
        font-weight: 600;
        font-size: $h4FS !important;
        margin-bottom: $h6FS;
        z-index: 10;
      }
      & .text{
        font-weight: 300;
        font-size: $h6FS;
        z-index: 10;
      }
    }

    .dataBlock3{
      &_b1:hover::after{
        background: linear-gradient(315deg, rgba(22, 25, 32, 0) 62.32%, #1E232E 69.95%, rgba(34, 53, 111, 0.56) 77.2%, rgba(16, 151, 187, 0.61) 88.43%, rgba(0, 255, 224, 0.92) 94.54%, rgba(0, 255, 224, 0.53) 97.75%);
      }
      &_b2:hover::after{
        background: linear-gradient(142deg, rgba(22, 25, 32, 0) 54.13%, rgba(30, 35, 46, 0.58) 64.18%, rgba(34, 53, 111, 0.6) 71.44%, rgba(16, 151, 187, 0.68) 80.68%, rgba(11, 182, 198, 0.774518) 83.61%, #00FFE0 90.59%);
      }
      &_b3:hover::after{
        background: linear-gradient(15deg, rgba(22, 25, 32, 0) 54.43%, #1E232E 71.89%, rgba(34, 53, 111, 0.56) 82.42%, rgba(16, 151, 187, 0.61) 89%, rgba(0, 255, 224, 0.92) 97.09%, rgba(0, 255, 224, 0.53) 101.34%);
      }
      &_b4:hover::after{
        background: linear-gradient(204.67deg, rgba(22, 25, 32, 0) 41.66%, #1E232E 59.64%, rgba(34, 53, 111, 0.56) 70.48%, rgba(16, 151, 187, 0.61) 77.26%, rgba(0, 255, 224, 0.92) 85.59%, rgba(0, 255, 224, 0.53) 89.96%);
      }
    }

    .wide {
      min-width:1125.5/1920*100%;
      border-right: 4px #14161B solid ;
      background-image: url('~/assets/images/pages/Main/block3/col1.svg');
      & .mainPage_block3_item{
        padding: 50px 118px;
      }
    }
    .tall {
      min-width: 617/1920*100%;
      border-left: 4px #14161B solid ;
      background-image: url('~/assets/images/pages/Main/block3/col3.svg');
      & .mainPage_block3_item{
        padding: 40px 30px;
      }
    }
    .middle{
      width:100%;
      border-bottom: 4px #14161B solid ;
      background-image: url('~/assets/images/pages/Main/block3/col2.svg');
      background-size: cover;
      background-position-y: bottom;
    }
  }
}
//  @import url('~/assets/scss/pages/mainPage/_block1.scss');
  // @import url('~/assets/scss/pages/mainPage/_main.scss');
</style>
