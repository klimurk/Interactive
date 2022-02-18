<template>
  <div>
    <div class="documentsPage">
      <v-img
        class="pageImgHead"
        :lazy-src="require('~/assets/images/sheets/Documents/head.png')"
        :src="require('~/assets/images/sheets/Documents/head.png')"
        width="96%"
        alt=""
      />
      <p class="textTitle">
        {{ datablock.title }}
      </p>
      <p class="text textSubtitle">
        {{ datablock.text }}
      </p>
      <div v-for="section in datablock.sections" :key="section.name" class="documentsPage_section">
        <div class="documentsPage_section_header" @click="section.isOpen = !section.isOpen">
          <p>{{ section.name }}</p>
          <button>
            +
          </button>
        </div>
        <div class="documentsPage_section_info" :class="{ sectionOpen:section.isOpen }">
          <p v-for="paragraph in section.paragraph" :key="paragraph.text">
            {{ paragraph.text }}
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
            paragraph:
            [
              {
                text: 'Eveniet Ave & 73th Street, Voluptates, NY 15432, USA'
              }
            ]
          },
          {
            name: 'Отказ от ответственности',
            isOpen: false,
            paragraph:
            [
              {
                text: 'Eveniet Ave & 73th Street, Voluptates, NY 15432, USA'
              }
            ]
          },
          {
            name: 'Клиентское соглашение',
            isOpen: false,
            paragraph:
            [
              {
                text: 'Eveniet Ave & 73th Street, Voluptates, NY 15432, USA'
              }
            ]
          },
          {
            name: 'Регламент осуществления неторговых операций',
            isOpen: false,
            paragraph:
            [
              {
                text: 'Eveniet Ave & 73th Street, Voluptates, NY 15432, USA'
              }
            ]
          },
          {
            name: 'Политика возврата',
            isOpen: false,
            paragraph:
            [
              {
                text: 'Eveniet Ave & 73th Street, Voluptates, NY 15432, USA'
              }
            ]
          },
          {
            name: 'Политика конфиденциальности',
            isOpen: false,
            paragraph:
            [
              {
                text: 'Eveniet Ave & 73th Street, Voluptates, NY 15432, USA'
              }
            ]
          },
          {
            name: 'Политика AML и KYC',
            isOpen: false,
            paragraph:
            [
              {
                text: 'Eveniet Ave & 73th Street, Voluptates, NY 15432, USA'
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
  methods: {
  }
}
</script>

<style lang="scss" scoped>
  .documentsPage{
    & .v-image{
      border-radius: 40px;
      margin: 30px auto 65px;
    }
    & .text{
      max-width: vwDesk(1629);
      margin: 25px auto 50px;
    }
    &_section{
      border-bottom: 2px solid #14161B;
      margin-bottom: 30px;
      &_header{
        @include makeitflex(row, space-between);
        width: vwDesk(800);
        margin: 0 auto;
        margin-bottom: 30px;
        transition: all $anim-time $anim-type;
        & >p{
          font-family: 'Raleway', sans-serif !important;
          font-style: normal !important;
          font-weight: bold !important;
          font-size: $fs-24 !important;
          text-transform: uppercase;
          transition: background $anim-time $anim-type;
        }
        & >button{
          font-size: $fs-36;
          transition: all $anim-time $anim-type;
        }
        &:hover{
          & >p{
            background: linear-gradient(180deg, #1CB0FF 0%, #0A87FA 100%);
            background-clip: text;
            -webkit-text-fill-color: transparent;
            cursor: pointer;
          }
          & >button{
            background: linear-gradient(180deg, #1CB0FF 0%, #0A87FA 100%);
            background-clip: text;
            -webkit-text-fill-color: transparent;
          }
        }
      }
      &_info{
        max-height: 0;
         transform: scaleY(0);
          transform-origin: top;
          transition: transform 0.26s ease;
        overflow: hidden;
        & >p{
          padding: 10px 40px;
        }
      }
    }
  }
  .sectionOpen{
    max-height:2000vh;
    transform: scaleY(1);
  }

</style>
