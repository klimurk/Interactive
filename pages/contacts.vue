<template>
  <div>
    <div class="contactsPage">
      <v-img
        lazy-src="/assets/images/pages/Contacts/head.png"
        :src="require('/assets/images/pages/Contacts/head.png')"
        width="96%"
        alt=""
      />
      <p class="title">
        {{ datablock.title }}
      </p>
      <p class="text">
        {{ datablock.text }}
      </p>
      <div class="accPage_blocks">
        <div v-for="button in datablock.buttons" :key="button.name" class="accPage_blocks_block">
          <div class="accPage_blocks_block_svg" v-html="button.svgImg" />
          <div class="accPage_blocks_name">
            {{ button.name }}
          </div>
          <div class="accPage_blocks_block_name_links">
            <a v-for="link in button.links" :key="link.href" :href="link.href">{{ link.text }}</a>
          </div>
        </div>
      </div>
      <div class="accPage_mapBlock">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d193595.91598020084!2d-74.12010717581643!3d40.69740302589478!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x89c24fa5d33f083b%3A0xc80b8f06e177fe62!2z0J3RjNGOLdCZ0L7RgNC6LCDQodCo0JA!5e0!3m2!1sru!2scz!4v1644014790181!5m2!1sru!2scz"
          width="600"
          height="450"
          style="border:0;"
          allowfullscreen=""
          loading="lazy"
        />
        <div class="accPage_mapBlock_data">
          <p class="text">
            {{ datablock.contactformData.text }}
          </p>
        </div>
        <div class="accPage_mapBlock_data_field">
          <p>{{ datablock.contactformData.name }}</p>
          <v-text-field single-line v-model="datablock.contactformData.inputs.name.text" type="text" :error="datablock.contactformData.inputs.name.valid" height="30px" />
        </div>
        <div class="accPage_mapBlock_data_field">
          <p>{{ datablock.contactformData.email }}</p>
          <v-text-field single-line v-model="datablock.contactformData.inputs.email.text" type="text" :error="datablock.contactformData.inputs.email.valid" height="10px" />
        </div>
        <div class="accPage_mapBlock_data_field big">
          <p>{{ datablock.contactformData.message }}</p>
          <v-textarea v-model="datablock.contactformData.inputs.message.text" type="text" :error="datablock.contactformData.inputs.message.valid" />
        </div>
        <button @click="sendform">
          {{ datablock.contactformData.btn_send }}
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  buildModules: ['nuxt-animejs'],
  name: 'AccountType',
  filters: {},
  components: {
    // SVGMail: () => import('~/components/svg/contacts/mail'),
    // SVGMap: () => import('~/components/svg/contacts/map'),
    // SVGPhone: () => import('~/components/svg/contacts/phone')
  },
  data () {
    return {
      datablock: {
        title: 'Контакты',
        text: 'InteractiveFund всегда заботится о своих клиентах. Наша команда делает все возможное чтобы направить вас, и помочь добиться успеха. Команда службы поддержки клиентов фонда всегда готова помогать вам 24 часа в сутки, 5 дней в неделю. ',
        buttons:
        [
          {
            name: 'Our Office',
            svgImg: '<SVGMail />',
            links:
            [
              {
                href: '',
                text: 'Eveniet Ave & 73th Street, Voluptates, NY 15432, USA'
              }
            ]
          },
          {
            name: 'Write Us',
            links:
            [
              {
                href: 'mailto:doubleemail@gmail.com',
                text: 'ouremail@gmail.com'
              },
              {
                href: 'mailto:doubleemail@gmail.com',
                text: 'doubleemail@gmail.com'
              }
            ]
          },
          {
            name: 'Support',
            svgImg: '',
            links:
            [
              {
                href: 'tel:+712395433564',
                text: '+7 123 954-33-564'
              }
            ]
          }
        ],
        contactformData: {
          text: 'Вы можете связаться с нами любым удобным для вас способом, или же заполнить форму обратной связи, которая находится ниже. Команда непрерывно работает, чтобы ответить вам в ближайшее время. В редких случаях высокой загруженности обработка запроса может занять до 24 часов.',
          name: 'Имя',
          email: 'Адрес эл. почты',
          message: 'Message',
          btn_send: 'Отправить',
          inputs: {
            name: {
              text: '',
              valid: true
            },
            email: {
              text: '',
              valid: true
            },
            message: {
              text: '',
              valid: true
            }
          }
        }
      }
    }
  },
  computed: {},
  watch: {},
  created () {},
  mounted () {},
  methods: {
    sendform () {
    }
  }
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
      // box-shadow: inset 0px 0px 24px rgba(13, 15, 18, 0.8);
      border-radius: 40px;
      margin: 50px 40px;
      padding: 33px;
      flex: 1 0 0;
      color: $textColor1;
      border: solid 2px #171B21;
      box-shadow: inset 0px 0px 24px #000000;
      @include makeitflex(row,center);
      position: relative;
      z-index: 1;
      & ::after{
        opacity: 0;
        border-radius: 40px;
        background-image: url('~/assets/images/pages/AccountsType/block_hover.svg');
        transition: opacity $transition_time linear !important ;
        // filter: blur(64px);
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
