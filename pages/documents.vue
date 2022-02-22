<template>
  <div>
    <div class="documents">
      <v-img
        class="pageImgHead"
        :lazy-src="require('~/assets/images/sheets/Documents/head.png')"
        :src="require('~/assets/images/sheets/Documents/head.png')"

        alt=""
      />
      <p class="bBigTitle documents__bBigTitle" :class="{'documents__bBigTitle--fs18-m':mobile}">
        {{ datablock.title }}
      </p>
      <p class="bSubTitle documents__bSubTitle" :class="{'documents__bSubTitle--fs14-m':mobile}">
        {{ datablock.text }}
      </p>
      <div v-for="section in datablock.sections" :key="section.name" class="section">
        <div class="section__header" @click="section.isOpen = !section.isOpen">
          <p class="bSubTitle link section__bSubTitle" :class="{'section__bSubTitle--fs14-m':mobile}">
            {{ section.name }}
          </p>
          <button class="bTitle btnPlus link">
            +
          </button>
        </div>
        <div class="section__info" :class="{ 'section__info--open':section.isOpen }">
          <p v-for="paragraph in section.paragraph" :key="paragraph" class="bSmallText section__bSmallText">
            {{ paragraph }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  buildModules: ['nuxt-animejs'],
  name: 'DocumentsPage',
  filters: {},
  components: {
  },
  data () {
    return {
      datablock: {
        title: 'Документы',
        text: 'Пожалуйста, прежде чем открывать счет и начинать торговлю ознакомьтесь с документацией ниже.',
        sections:
        [
          {
            name: 'Юридическая информация',
            isOpen: false,
            paragraph: ['Eveniet Ave & 73th Street, Voluptates, NY 15432, USA']
          },
          {
            name: 'Отказ от ответственности',
            isOpen: false,
            paragraph: ['Eveniet Ave & 73th Street, Voluptates, NY 15432, USA']
          },
          {
            name: 'Клиентское соглашение',
            isOpen: false,
            paragraph: ['Eveniet Ave & 73th Street, Voluptates, NY 15432, USA']
          },
          {
            name: 'Регламент осуществления неторговых операций',
            isOpen: false,
            paragraph: ['Eveniet Ave & 73th Street, Voluptates, NY 15432, USA']
          },
          {
            name: 'Политика возврата',
            isOpen: false,
            paragraph: ['Eveniet Ave & 73th Street, Voluptates, NY 15432, USA']
          },
          {
            name: 'Политика конфиденциальности',
            isOpen: false,
            paragraph: ['Eveniet Ave & 73th Street, Voluptates, NY 15432, USA']
          },
          {
            name: 'Политика AML и KYC',
            isOpen: false,
            paragraph: ['Eveniet Ave & 73th Street, Voluptates, NY 15432, USA']
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
  methods: {
  }
}
</script>

<style lang="scss" scoped>
  .documents{
    @media(max-width:$w-adapt){
      padding: 0 vwMob(35) vwMob(25);
    }
    &__bBigTitle{
      text-align: center;
      @media(max-width:$w-adapt){
        margin-bottom: vwMob(10);
      }
      &--fs18-m{
        font-size: $fs-18-m;
      }
    }
    &__bSubTitle{
      // max-width: vwDesk(1629);
      text-align: center;
      margin: vwDesk(25) auto vwDesk(50);
      @media(max-width:$w-adapt){
        margin: 0 0 vwMob(25);
      }
      &--fs14-m{
        font-size: $fs-14-m;
      }
    }
    .section{
      border-bottom: 2px solid #14161B;
      margin-bottom: vwDesk(30);
      @media(max-width:$w-adapt){
        margin-bottom: vwMob(50);
        border-bottom: 2px solid $clr-text-1;
      }
      &__bSubTitle{
        // font-family: 'Raleway', sans-serif !important;
        // font-style: normal !important;
        font-weight: bold !important;
        // font-size: $fs-24 !important;
        text-transform: uppercase;
        transition: background $anim-time $anim-type;
        &--fs14-m{
          font-size: $fs-14-m;
        }
      }
      &__header{
        @include makeitflex(row, space-between);
        width: vwDesk(800);
        margin: 0 auto;
        margin-bottom: vwDesk(30);
        transition: all $anim-time $anim-type;
        @media(max-width:$w-adapt){
          width: 100%;
        }
      }
      .btnPlus{
        font-size: $fs-36;
        transition: all $anim-time $anim-type;
        @media(max-width:$w-adapt){
          font-weight: normal;
          font-size: $fs-18-m;
          width: vwMob(15);
        }
      }
        // &:hover{
        //   & >p{
        //     background: linear-gradient(180deg, #1CB0FF 0%, #0A87FA 100%);
        //     background-clip: text;
        //     -webkit-text-fill-color: transparent;
        //     cursor: pointer;
        //   }
        //   & >button{
        //     background: linear-gradient(180deg, #1CB0FF 0%, #0A87FA 100%);
        //     background-clip: text;
        //     -webkit-text-fill-color: transparent;
        //   }
        // }
      &__info{
        max-height: 0;
        transform: scaleY(0);
        transform-origin: top;
        transition: transform 0.26s ease;
        overflow: hidden;
        &--open{
          max-height:2000vh;
          transform: scaleY(1);
        }
      }
      &__bSmallText{
        padding:  vwDesk(40);
      }
    }
  }

</style>
