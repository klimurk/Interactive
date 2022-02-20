<template>
  <div>
    <div class="acc">
      <v-img
        class="pageImgHead"
        lazy-src="/assets/images/sheets/AccountsType/head.png"
        :src="require('/assets/images/sheets/AccountsType/head.png')"

        alt=""
      />
      <p class="bBigTitle acc__bBigTitle" :class="{'acc__bBigTitle--fs18':mobile}">
        {{ datablock.title }}
      </p>
      <p class="bSubTitle acc__bSubTitle " :class="{'acc__bSubTitle--fw':mobile}">
        {{ datablock.text }}
      </p>
      <div v-for="block in datablock.blocks" :key="block.colPrice.price" class="accBlock">
        <div class="accBlock__col">
          <div class="bSubTitle accBlock__bSubTitle" :class="{'acc__bSubTitle--fs18':mobile}">
            {{ block.colPrice.type }}
          </div>
          <div class="bBigTitle accBlock__bBigTitle accBlock__bBigTitle--fs40" :class="{'accBlock__bBigTitle--fs24':mobile}">
            {{ block.colPrice.symbol }}{{ block.colPrice.price }}
          </div>
        </div>
        <div v-for="col in block.colText" :key="col.txt1" class="accBlock__col">
          <p v-for="text in col.text" :key="text" class="bSmallText accBlock__bSmallText" :class="{'accBlock__bSmallText--fs14':mobile}">
            {{ text }}
          </p>
        </div>
        <div class="accBlock__col">
          <button class="accBlock__btnBlue btnBlue">
            {{ datablock.btn_text }}
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  buildModules: ['nuxt-animejs'],
  name: 'AccountType',
  filters: {},
  data () {
    return {
      datablock: {
        title: 'Типы счетов',
        text: 'InteractiveFund предоставляет своим клиентам различные типы счетов, которые позволяют выбрать самый выгодный вариант для вашей торговой стратегии.',
        btn_text: 'Открыть счет',
        blocks:
        [
          {
            colPrice:
            {
              type: 'Basic',
              price: 1000,
              symbol: '$'
            },
            colText:
            [
              {
                text: ['Кредитное плечо до 1:500', 'Вводное обучение от финансового управляющего', 'Круглосуточная поддержка клиентов']
              },
              {
                text: ['Сопровождение счёта финансовым управляющим', 'Плавающий спред', 'Формирование и модерация группы основных торговых инструментов']
              },
              {
                text: ['Создание индивидуального бизнес-плана', 'Создание уникальной торговой стратегии', 'Торговые сигналы класса ВВВ']
              }
            ]
          },
          {
            colPrice:
            {
              type: 'Standart',
              price: 5000,
              symbol: '$'
            },
            colText:
            [
              {
                text: ['Кредитное плечо до 1:500', 'Вводное обучение от финансового управляющего', 'Круглосуточная поддержка клиентов']
              },
              {
                text: ['Сопровождение счёта финансовым управляющим', 'Плавающий спред', 'Формирование и модерациягруппы основных торговых инструментов']
              },
              {
                text: ['Создание индивидуального бизнес-плана ', 'Создание уникальной торговой стратегии', 'Торговые сигналы класса ВВA']
              }
            ]
          },
          {
            colPrice:
            {
              type: 'PREMIUM ',
              price: 25000,
              symbol: '$'
            },
            colText:
            [
              {
                text: ['Кредитное плечо до 1:500', 'Вводное обучение от финансового управляющего', 'Круглосуточная поддержка клиентов']
              },
              {
                text: ['Сопровождение счёта финансовым управляющим', 'Плавающий спред', 'Формирование и модерация группы основных торговых инструментов']
              },
              {
                text: ['Создание индивидуального бизнес-плана', 'Создание уникальной торговой стратегии', 'Торговые сигналы класса ВAA']
              }
            ]
          },
          {
            colPrice:
            {
              type: 'Vip',
              price: 50000,
              symbol: '$'
            },
            colText:
            [
              {
                text: ['Кредитное плечо до 1:500', 'Вводное обучение от финансового управляющего', 'Круглосуточная поддержка клиентов']
              },
              {
                text: ['Сопровождение счёта финансовым управляющим', 'Плавающий спред', 'Формирование и модерация группы основных торговых инструментов']
              },
              {
                text: ['Создание индивидуального бизнес-плана', 'Создание уникальной торговой стратегии', 'Торговые сигналы класса AAA']
              }
            ]
          }
        ]
      }
    }
  },
  computed: {
    mobile () {
      return this.$vuetify.breakpoint.sm || this.$vuetify.breakpoint.xs
    }
  },
  watch: {},
  created () {},
  mounted () {},
  methods: {}
}
</script>

<style lang="scss" scoped>
  .acc{
    &__bBigTitle{
      text-align: center;
      &--fs18{
        font-size: $fs-18-m;
      }
    }
    &__bSubTitle{
      max-width: vwDesk(1075);
      margin: vwDesk(25) auto 0;
      text-align: center;
      @media(max-width:$w-adapt){
        max-width: vwMob(340);
        margin: vwMob(14) auto;
      }
      &--fw{
        font-weight: 700;
      }
    }
  }
  .accBlock{
      background: linear-gradient(107.15deg, rgba(29, 30, 32, 0.93) 0%, rgba(13, 21, 34, 0.93) 100%);
      border-radius: vwDesk(40);
      margin: vwDesk(50) vwDesk(40);
      padding: vwDesk(30);
      flex: 1 0 0;
      color: $clr-text-1;
      border: solid 2px #171B21;
      box-shadow: inset 0px 0px 24px #000000;
      @include makeitflex(row,center);
      position: relative;
      z-index: 1;
      @media(max-width:$w-adapt){
        @include makeitflex(column,flex-start);
        width: vwMob(235);
        margin: 0 auto vwMob(40);
        padding: vwMob(20) vwMob(15);
        border-radius: vwMob(20);
      }
      & ::after{
        opacity: 0;
        border-radius: vwDesk(40);
        background-image: url('~/assets/images/sheets/AccountsType/block_hover.svg');
        background-size: cover;
        transition: opacity $anim-time $anim-type !important ;
        position: absolute;
        left: 0;
        top: 0;
        width: 100%;
        height: 100%;
        z-index: -1;
        content: '';
      }
      & :hover ::after{
        opacity: 1;
      }
      &__bSubTitle{
        @media(max-width:$w-adapt){
          text-align: center;
          margin-bottom: vwMob(15);
        }
        // font-family: 'Manrope', sans-serif !important;
        // font-style: normal;
        // font-weight: bold;
        // font-size: $fs-24;
        // line-height: 32/24*1;
        &--fs18{
          font-size: $fs-18-m;
        }
      }
      &__bBigTitle{
        @media(max-width:$w-adapt){
          text-align: center;
          margin-bottom: vwMob(20);
        }
        &--fs40{
          font-size: $fs-40;
        }
        &--fs24{
          font-size: $fs-24-m;
        }
      }
      &__btnBlue{
        text-align: center;
        height: fit-content;
        padding: vwDesk(12) vwDesk(30);
        @media(max-width:$w-adapt){
          padding: vwMob(15) vwMob(30);
          margin: vwMob(30) auto 0;
          width: vwMob(170);
        }
      }
      &__col{
        margin: 0 vwDesk(20);
        width: vwDesk(220);
        @include makeitflex(column, center);
        @media(max-width:$w-adapt){
          width: 100%;
        }
      }
      &__bSmallText{
        flex: 1 0 0;
        margin: vwDesk(10) 0;
        @media(max-width:$w-adapt){
          margin: vwMob(7) 0;
        }
        &--fs14{
          font-size: $fs-14-m;
          font-weight: normal;
        }
      }
    }
</style>
