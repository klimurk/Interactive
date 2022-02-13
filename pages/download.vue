<template>
  <div>
    <div class="downloadPage">
      <v-img
        class="pageImgHead"
        :lazy-src="require('~/assets/images/sheets/download/head.png')"
        :src="require('~/assets/images/sheets/download/head.png')"
        width="96%"
        alt=""
      />
      <div class="block1">
        <v-img
          class="infoImg"
          :lazy-src="require('~/assets/images/sheets/download/notebook.png')"
          :src="require('~/assets/images/sheets/download/notebook.png')"
          alt=""
        />
        <div class="infoBlock">
          <p class="title">
            {{ info[0].title }}
          </p>
          <p class="text">
            {{ info[0].text }}
          </p>
          <div class="block_buttons">
            <button class="btn_download btn_blue">
              {{ info[0].btn1Text }}
              <svg viewBox="0 0 18 20">
                <path d="M0.671875 9.19824V3.94824L6.67188 2.62824V9.10824L0.671875 9.19824ZM17.6719 0.198242V8.94824L7.67188 9.09824V2.40824L17.6719 0.198242ZM0.671875 10.1982L6.67188 10.2882V17.0982L0.671875 15.9482V10.1982ZM17.6719 10.4482V19.1982L7.67188 17.2882V10.2982L17.6719 10.4482Z" fill="white" />
              </svg>
            </button>
            <button class="btn_download btn_apple">
              {{ info[0].btn2Text }}
              <svg viewBox="0 0 17 21">
                <path d="M15.0565 18.189C14.2265 19.429 13.3465 20.639 12.0065 20.659C10.6665 20.689 10.2365 19.869 8.71653 19.869C7.18653 19.869 6.71653 20.639 5.44653 20.689C4.13653 20.739 3.14653 19.369 2.30653 18.159C0.596528 15.689 -0.713473 11.139 1.04653 8.07897C1.91653 6.55897 3.47653 5.59897 5.16653 5.56896C6.44653 5.54896 7.66653 6.43896 8.45653 6.43896C9.23653 6.43896 10.7165 5.36897 12.2665 5.52896C12.9165 5.55897 14.7365 5.78896 15.9065 7.50896C15.8165 7.56896 13.7365 8.78897 13.7565 11.319C13.7865 14.339 16.4065 15.349 16.4365 15.359C16.4065 15.429 16.0165 16.799 15.0565 18.189ZM9.34653 2.18896C10.0765 1.35896 11.2865 0.728965 12.2865 0.688965C12.4165 1.85896 11.9465 3.03896 11.2465 3.87896C10.5565 4.72896 9.41653 5.38897 8.29653 5.29896C8.14653 4.14896 8.70653 2.94896 9.34653 2.18896Z" fill="white" />
              </svg>
            </button>
          </div>
        </div>
        <div class="infoBlock">
          <p class="title">
            {{ info[1].title }}
          </p>
          <p class="text">
            {{ info[1].text }}
          </p>
          <div class="block_buttons">
            <button class="btn_download btn_blue">
              {{ info[1].btn1Text }}
              <svg viewBox="0 0 19 21">
                <path d="M0.914062 19.1996V2.19961C0.914062 1.60961 1.25406 1.08961 1.75406 0.849609L11.6041 10.6996L1.75406 20.5496C1.25406 20.2996 0.914062 19.7896 0.914062 19.1996ZM14.7241 13.8196L3.96406 20.0396L12.4541 11.5496L14.7241 13.8196ZM18.0741 9.50961C18.4141 9.77961 18.6641 10.1996 18.6641 10.6996C18.6641 11.1996 18.4441 11.5996 18.0941 11.8796L15.8041 13.1996L13.3041 10.6996L15.8041 8.19961L18.0741 9.50961ZM3.96406 1.35961L14.7241 7.57961L12.4541 9.84961L3.96406 1.35961Z" fill="white" />
              </svg>
            </button>
            <button class="btn_download btn_apple">
              {{ info[1].btn2Text }}
              <svg viewBox="0 0 17 21">
                <path d="M15.0565 18.189C14.2265 19.429 13.3465 20.639 12.0065 20.659C10.6665 20.689 10.2365 19.869 8.71653 19.869C7.18653 19.869 6.71653 20.639 5.44653 20.689C4.13653 20.739 3.14653 19.369 2.30653 18.159C0.596528 15.689 -0.713473 11.139 1.04653 8.07897C1.91653 6.55897 3.47653 5.59897 5.16653 5.56896C6.44653 5.54896 7.66653 6.43896 8.45653 6.43896C9.23653 6.43896 10.7165 5.36897 12.2665 5.52896C12.9165 5.55897 14.7365 5.78896 15.9065 7.50896C15.8165 7.56896 13.7365 8.78897 13.7565 11.319C13.7865 14.339 16.4065 15.349 16.4365 15.359C16.4065 15.429 16.0165 16.799 15.0565 18.189ZM9.34653 2.18896C10.0765 1.35896 11.2865 0.728965 12.2865 0.688965C12.4165 1.85896 11.9465 3.03896 11.2465 3.87896C10.5565 4.72896 9.41653 5.38897 8.29653 5.29896C8.14653 4.14896 8.70653 2.94896 9.34653 2.18896Z" fill="white" />
              </svg>
            </button>
          </div>
        </div>
        <v-img
          class="infoImg"
          style="margin-top:-5vw"
          :lazy-src="require('~/assets/images/sheets/download/mobile.png')"
          :src="require('~/assets/images/sheets/download/mobile.png')"
          alt=""
        />
        <svg viewBox="0 0 1920 995">
          <mask
            id="mask0_557_16"
            style="mask-type:alpha"
            maskUnits="userSpaceOnUse"
            x="0"
            y="0"
            width="1920"
            height="995"
          >
            <rect width="1920" height="995" fill="#C4C4C4" />
          </mask>
          <g mask="url(#mask0_557_16)">
            <mask
              id="mask1_557_16"
              style="mask-type:alpha"
              maskUnits="userSpaceOnUse"
              x="-11"
              y="1"
              width="1921"
              height="1077"
            >
              <rect
                x="-10.0234"
                y="1"
                width="1920"
                height="1077"
                fill="black"
                fill-opacity="0.9"
              />
            </mask>
            <g mask="url(#mask1_557_16)">
              <rect
                x="-10.0234"
                y="1"
                width="1920"
                height="1077"
                fill="url(#paint0_radial_557_16)"
                fill-opacity="0.4"
              />
            </g>
          </g>
          <defs>
            <radialGradient
              id="paint0_radial_557_16"
              cx="0"
              cy="0"
              r="1"
              gradientUnits="userSpaceOnUse"
              gradientTransform="translate(1413.53 632.585) rotate(174.342) scale(1011.49 698.524)"
            >
              <stop stop-color="#00FFE0" />
              <stop offset="0.229167" stop-color="#1097BB" stop-opacity="0.68" />
              <stop offset="0.515625" stop-color="#22356F" stop-opacity="0.6" />
              <stop offset="0.796875" stop-color="#1E232E" stop-opacity="0.58" />
              <stop offset="1" stop-color="#161920" stop-opacity="0" />
            </radialGradient>
          </defs>
        </svg>
      </div>
      <p class="underline">
        {{ underline }}
        <a href="">
          {{ underlineLink }}
        </a>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  buildModules: ['nuxt-animejs'],
  name: 'DownloadPage',
  filters: {},
  components: {
    // joinblock: () => import('~/components/joinBlock')
  },
  data () {
    return {
      info:
      [
        {
          title: 'MetaTrader 5 Desktop',
          text: 'Имея доступ к трем различным типам графиков, девяти таймфреймам, более пятидесяти предустановленным техническим индикаторам и полностью настраиваемому интерфейсу, MetaTrader 5 дает вам возможность точно отслеживать рынки.',
          btn1Text: 'Скачать для Windows',
          btn2Text: 'Скачать для MacOS'
        },
        {
          title: 'MetaTrader 5 Mobile',
          text: 'С Interactive-Fund MT5 Mobile вы можете пользоваться самой популярной торговой платформой на своем мобильном телефоне в любом месте и в любое время. Доступно для iOS и Android.',
          btn1Text: 'Google play',
          btn2Text: 'Appstore'
        }
      ],
      underline: 'Risk Warning: Derivatives are complex instruments and come with a high risk of losing money rapidly due to leverage. Between 74-89% of retail investor accounts lose money when trading Derivatives. You should consider whether you understand how Derivatives work and whether you can afford to take the high risk of losing your money. ',
      underlineLink: 'Please read our full Risk Disclosure.'
    }
  },
  computed: {},
  watch: {},
  created () {},
  mounted () {
  },
  beforeDestroy () {
  },
  methods: {
  }
}
</script>

<style lang="scss" scoped>
.downloadPage{
  .block1{
    @include makeitflex(row, space-between);
    flex-wrap: wrap;
    padding: 60/1920*100vw 50/1920*100vw 0;
    // padding: 0 ;
    position: relative;
    z-index: 1;
    >svg{
      position: absolute;
      width: 100%;
      bottom: 0;
      right: 0;
      z-index: -1;
    }
    .infoImg{
      max-width: 700/1920*100vw;
      margin-bottom: 90/1920*100vw;
      margin-right: 115/1920*100vw;
    }
    .infoBlock{
      max-width: 962/1920*100vw;
      .title{
        font-family: 'Manrope', sans-serif !important;
        font-style: normal !important;
        font-weight: bold !important;
        font-size: $h5FS !important;
        line-height: 100%;
        /* identical to box height, or 24px */

        letter-spacing: 0.05em;
        text-transform: uppercase;
        margin-bottom: 40px;
        background: linear-gradient(171.27deg, rgba(16, 151, 187, 0.68) -63.67%, #00FFE0 98.46%),linear-gradient(0deg, #FFFFFF, #FFFFFF);
        background-clip: text;
        -webkit-text-fill-color: transparent;
      }
      .text{
        font-family: 'Manrope', sans-serif !important;
        font-style: normal !important;
        font-weight: bold !important;
        font-size: $h5FS !important;
        line-height: 100%;
        /* identical to box height, or 24px */

        letter-spacing: 0.05em;
        margin-bottom: 70px;
      }
      .block_buttons{
        @include makeitflex(row, flex-start);
        .btn_download{
          @include makeitflex(row, flex-start);
          padding: 16px 30px;
          margin-right: 70/1920*100vw;
          text-transform: uppercase;
          >svg{
            width: 24/1920*100vw;
            height: 24/1920*100vw;
            margin-left: 16/1920*100vw;
          }
        }
      }
    }

  }
  .underline{
    font-family: 'Manrope', sans-serif !important;
    font-style: normal !important;
    font-weight: normal !important;
    font-size: $h7FS !important;
    line-height: 100%;
    /* or 14px */

    text-align: center;
    letter-spacing: 0.05em;
    text-transform: uppercase;
    max-width: 1840/1920*100vw;
    margin: 0 auto;
    margin-bottom: 75/1920*100vw;
    >a{
      background: linear-gradient(174.33deg, #29649B 2.19%, #00FDDF 99.09%), linear-gradient(0deg, #FFFFFF, #FFFFFF);
      background-clip: text;
      -webkit-text-fill-color: transparent;
      cursor: pointer;
      // position: relative;
      // transition: opacity $transition_time $transition_anim_type;
      // z-index: 1;
      // &:hover{
      //   background: linear-gradient(174.33deg, #29649B 2.19%, #00FDDF 99.09%), linear-gradient(0deg, #FFFFFF, #FFFFFF);
      // }
      // &:hover::after{
      //   opacity: 1;
      // }
      // &::after{
      //   z-index: -1;
      //   content: '';
      //   width: 100%;
      //   height: 100%;
      //   position: absolute;
      //   left: 0;
      //   top: 0;
      //   opacity: 0;
      //   background: rgba(19, 155, 253, 0.8);
      // }
    }
  }

}
</style>
