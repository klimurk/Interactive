<template>
  <div>
    <div class="contactsPage">
      <v-img
        class="pageImgHead"
        :lazy-src="require('~/assets/images/sheets/Contacts/head.png')"
        :src="require('~/assets/images/sheets/Contacts/head.png')"

        alt=""
      />
      <p class="textTitle">
        {{ datablock.title }}
      </p>
      <p class="text textSubtitle">
        {{ datablock.text }}
      </p>
      <div class="contactsPage_blocks">
        <div v-for="button in datablock.buttons" :key="button.name" class="contactsPage_blocks_block">
          <div class="contactsPage_blocks_block_svg">
            <SVGMail v-if=" button.svgImg === 'SVGMail' " />
            <SVGMap v-if=" button.svgImg === 'SVGMap' " />
            <SVGPhone v-if=" button.svgImg === 'SVGPhone' " />
          </div>
          <p class="contactsPage_blocks_block_name">
            {{ button.name }}
          </p>
          <div class="contactsPage_blocks_block_links">
            <a v-for="link in button.links" :key="link.href" :href="link.href">{{ link.text }}</a>
          </div>
        </div>
      </div>
      <div class="contactsPage_mapBlock">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d193595.91598020084!2d-74.12010717581643!3d40.69740302589478!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x89c24fa5d33f083b%3A0xc80b8f06e177fe62!2z0J3RjNGOLdCZ0L7RgNC6LCDQodCo0JA!5e0!3m2!1sru!2scz!4v1644014790181!5m2!1sru!2scz"
          style="border:0;"
          allowfullscreen=""
          loading="lazy"
        />
        <div class="contactsPage_mapBlock_data">
          <p class="text">
            {{ datablock.contactformData.text }}
          </p>
          <div class="contactsPage_mapBlock_data_field">
            <p>{{ datablock.contactformData.name }}</p>
            <v-text-field v-model="datablock.contactformData.inputs.name" :rules="[datablock.contactformData.inputs.rules.required]" outlined type="text" height="30px" />
          </div>
          <div class="contactsPage_mapBlock_data_field">
            <p>{{ datablock.contactformData.email }}</p>
            <v-text-field
              v-model="datablock.contactformData.inputs.email"
              :rules="[datablock.contactformData.inputs.rules.required, datablock.contactformData.inputs.rules.email]"
              counter
              maxlength="50"
              outlined
              type="text"
              height="10px"
            />
          </div>
          <div class="contactsPage_mapBlock_data_field big">
            <p>{{ datablock.contactformData.message }}</p>
            <v-textarea v-model="datablock.contactformData.inputs.message" outlined type="text" />
          </div>
          <button class="btnBlue" @click="sendform">
            {{ datablock.contactformData.btn_send }}
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  buildModules: ['nuxt-animejs'],
  name: 'ContactsPage',
  filters: {},
  components: {
    SVGMail: () => import('~/components/svg/contacts/mail'),
    SVGMap: () => import('~/components/svg/contacts/map'),
    SVGPhone: () => import('~/components/svg/contacts/phone')
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
            svgImg: 'SVGMap',
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
            svgImg: 'SVGMail',
            links:
            [
              {
                href: 'mailto:ouremail@gmail.com',
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
            svgImg: 'SVGPhone',
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
            name: '',
            email: '',
            message: '',
            rules: {
              required: value => !!value || 'Required.',
              email: (value) => {
                const pattern = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/
                return pattern.test(value) || 'Invalid e-mail.'
              }
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
      this.$axios.post('/8d343f77-dcfa-4e82-a1ca-87eda8f4872a', this.inputs).then((resp) => {

        // otvet
        // resp.
      }).catch((resp) => {

      })
    }
  }
}
</script>

<style lang="scss" scoped>
  .contactsPage{
    & .v-image{
      border-radius: 40px;
      margin: 30px auto 65px;
    }
    & .text{

      max-width: vwDesk(1629);
      margin: 25px auto 0;
    }
    &_blocks{
      @include makeitflex(row, center);
      margin: 30px auto ;
      &_block{
        @include makeitflex(column, flex-start);
        background: linear-gradient(107.15deg, rgba(29, 30, 32, 0.93) 0%, rgba(13, 21, 34, 0.93) 100%);
        border-radius: 40px;
        margin: 0 25px;
        padding: 15px 25px 20px;
        color: $clr-text-1;
        border: solid 2px #171B21;
        max-width: vwDesk(250);
        box-shadow: inset 0px 0px 24px #000000;
        background: linear-gradient(150deg, #333842 2.08%, #161B21 69.91%), #333842;
        border-radius: 30px;
        filter: drop-shadow(0px 100px 80px rgba(0, 0, 0, 0.19)) drop-shadow(0px 41.7776px 33.4221px rgba(0, 0, 0, 0.136582)) drop-shadow(0px 22.3363px 17.869px rgba(0, 0, 0, 0.11326)) drop-shadow(0px 12.5216px 10.0172px rgba(0, 0, 0, 0.095)) drop-shadow(0px 6.6501px 5.32008px rgba(0, 0, 0, 0.0767396)) drop-shadow(0px 2.76726px 2.21381px rgba(0, 0, 0, 0.0534177));
        flex: 1 0 0;
        &_svg{
          margin: 0 auto 10px ;
          height: 35px;
        }
        &_name{
          font-family: 'Manrope', sans-serif !important;
          font-style: normal !important;
          font-weight: bold !important;
          font-size: $fs-14 !important;
          line-height: 2.29 !important;
          text-align: center !important;

        }
        &_links{
          @include makeitflex(column, flex-start);
          font-family: 'Manrope', sans-serif !important;
          font-style: normal !important;
          font-weight: 600 !important;
          font-size: $fs-14 !important;
          // line-height: 2.29 !important;
          text-align: center;
          & >a{
            color: $clr-text-1 !important;
            transition: color $anim-time $anim-type;
            word-wrap: break-word;
            &:hover{
              cursor: pointer;
              color: $clr-btn-1 !important;
            }
          }
        }

      }
    }
    &_mapBlock{
      @include makeitflex(row, space-between);
      margin: 0 40px 50px;
      border-radius: 40px;
      background: #171B21;
      overflow: hidden;
      >iframe{
        height: auto;
        width: 754/1840 * 100% ;
      }
      &_data{
        padding: 45px 90px;
        width: (1840 - 754)/1840 * 100%;
        @include makeitflex(column, flex-start);
        .text{
          font-family: 'Manrope', sans-serif !important;
          font-style: normal !important;
          font-weight: normal !important;
          font-size: $fs-24 !important;
          line-height: 30/24*1 !important;
          text-align: left;
          margin-bottom: 45px;
        }
        &_field{
          & >p{
          font-family: 'Manrope', sans-serif !important;
            font-style: normal !important;
            font-weight: 500 !important;
            font-size: $fs-18 !important;
            line-height: 1.3;
          }
        }
        & >button{
          text-align: right;
          padding: 16px 40px;
          font-family: 'Manrope', sans-serif !important;
          font-style: normal!important;
          font-weight: 600 !important;
          font-size: $fs-14 !important;
          line-height: 19/14*1;
          letter-spacing: 0.05em;
          text-transform: uppercase !important ;
          margin-left: auto;
        }
      }
    }
  }

</style>
