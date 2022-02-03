<template>
  <div>
    <div class="accPage">
      <v-img
        lazy-src="/assets/images/pages/AccountsType/head.png"
        :src="require('/assets/images/pages/AccountsType/head.png')"
        width="96%"
        alt=""
      />
      <p class="title">
        {{ datablock.title }}
      </p>
      <p class="text">
        {{ datablock.text }}
      </p>
      <div v-for="block in datablock.blocks" :key="block.colPrice.price" class="accPage_block">
        <div class="accPage_block_col">
          <div class="accPage_block_col_type">
            {{ block.colPrice.type }}
          </div>
          <div class="accPage_block_col_price">
            {{ block.colPrice.symbol }}{{ block.colPrice.price }}
          </div>
        </div>
        <div v-for="col in block.colText" :key="col.txt1" class="accPage_block_col">
          <p>{{ col.txt1 }}</p>
          <p>{{ col.txt2 }}</p>
          <p>{{ col.txt3 }}</p>
        </div>
        <div class="accPage_block_col">
          <button class="accPage_block_col_btn btn_blue">
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
                txt1: 'Кредитное плечо до 1:500',
                txt2: 'Вводное обучение от финансового управляющего',
                txt3: 'Круглосуточная поддержка клиентов'
              },
              {
                txt1: 'Сопровождение счёта финансовым управляющим',
                txt2: 'Плавающий спред',
                txt3: 'Формирование и модерация группы основных торговых инструментов'
              },
              {
                txt1: 'Создание индивидуального бизнес-плана',
                txt2: 'Создание уникальной торговой стратегии',
                txt3: 'Торговые сигналы класса ВВВ'
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
                txt1: 'Кредитное плечо до 1:500',
                txt2: 'Вводное обучение от финансового управляющего',
                txt3: 'Круглосуточная поддержка клиентов'
              },
              {
                txt1: 'Сопровождение счёта финансовым управляющим',
                txt2: 'Плавающий спред',
                txt3: 'Формирование и модерациягруппы основных торговых инструментов'
              },
              {
                txt1: 'Создание индивидуального бизнес-плана ',
                txt2: 'Создание уникальной торговой стратегии',
                txt3: 'Торговые сигналы класса ВВA'
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
                txt1: 'Кредитное плечо до 1:500',
                txt2: 'Вводное обучение от финансового управляющего',
                txt3: 'Круглосуточная поддержка клиентов'
              },
              {
                txt1: 'Сопровождение счёта финансовым управляющим',
                txt2: 'Плавающий спред',
                txt3: 'Формирование и модерация группы основных торговых инструментов'
              },
              {
                txt1: 'Создание индивидуального бизнес-плана',
                txt2: 'Создание уникальной торговой стратегии',
                txt3: 'Торговые сигналы класса ВAA'
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
                txt1: 'Кредитное плечо до 1:500',
                txt2: 'Вводное обучение от финансового управляющего',
                txt3: 'Круглосуточная поддержка клиентов'
              },
              {
                txt1: 'Сопровождение счёта финансовым управляющим',
                txt2: 'Плавающий спред',
                txt3: 'Формирование и модерация группы основных торговых инструментов'
              },
              {
                txt1: 'Создание индивидуального бизнес-плана',
                txt2: 'Создание уникальной торговой стратегии',
                txt3: 'Торговые сигналы класса AAA'
              }
            ]
          }
        ]
      }
    }
  },
  computed: {},
  watch: {},
  created () {},
  mounted () {},
  methods: {}
}
</script>

<style lang="scss" scoped>
  .accPage{
    & .v-image{
      border-radius: 40px;
      margin: 30px auto 65px;
    }
    & .title{
      font-family: 'Manrope', sans-serif !important;
      font-style: normal;
      font-weight: 800 !important;
      font-size: $h2FS !important;
      text-align: center;
      letter-spacing: 0.05em !important;
    }
    & .text{
      font-family: 'Manrope', sans-serif !important;
      font-style: normal;
      font-weight: 700 !important;
      font-size: $h5FS !important;
      // line-height: 100% !important;
      text-align: center;
      letter-spacing: 0.05em !important;
      max-width: 1075/1920*100vw;
      margin: 25px auto 0;
    }
    &_block{
      background: linear-gradient(107.15deg, rgba(29, 30, 32, 0.93) 0%, rgba(13, 21, 34, 0.93) 100%);
      box-shadow: inset 0px 0px 24px rgba(13, 15, 18, 0.8);
      border-radius: 40px;
      margin: 50px 40px;
      padding: 33px;
      flex: 1 0 0;
      color: $textColor1;
      border: solid 2px #171B21;
      box-shadow: inset 0px 0px 24px #000000;
      @include makeitflex(row,center);
      &:hover{
      }
      &_col{
        margin: 0 20px;
        // flex: 1 0 0;
        width: 220/1920*100vw;
        @include makeitflex(column, center);
        &_type{
          font-family: 'Manrope', sans-serif !important;
          font-style: normal;
          font-weight: bold;
          font-size: $h5FS;
          line-height: 32/24*1;
        }
        &_price{
          font-family: 'Manrope', sans-serif !important;
          font-style: normal;
          font-weight: bold;
          font-size: $h3FS;
          line-height: 48/40*1;
        }
        &_btn{
          font-family: 'Roboto', sans-serif !important;
          font-style: normal !important;
          font-weight: bold !important;
          font-size: $h6FS;
          line-height: 1.5;
          text-align: center;
          height: fit-content;
          padding: 12px 30px;
        }
        >p{
          font-family: 'Manrope', sans-serif !important;
          font-style: normal !important;
          font-weight: normal !important;
          font-size: $h7FS !important;
          line-height: 1 !important;
          flex: 1 0 0;
          margin: 10px 0;
        }
      }
    }
  }
</style>
