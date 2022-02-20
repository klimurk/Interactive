<template>
  <v-app>
    <header v-click-outside="nav_reset" class="header">
      <NuxtLink class="bSubTitle link header__bSubTitle header__bSubTitle--big" to="/" @click="nav_reset">
        <svg class="header__svg" viewBox="0 0 89 52">
          <circle cx="26" cy="26" r="26" />
          <path
            d="M63 2.6782e-06C69.8956 2.37678e-06 76.5088 2.73928 81.3848 7.61522C86.2607 12.4912 89 19.1044 89 26C89 32.8956 86.2607 39.5088 81.3848 44.3848C76.5088 49.2607 69.8956 52 63 52L63 26L63 2.6782e-06Z"
          />
        </svg>
        <p>Lorem ipsum</p>
      </NuxtLink>
      <div class="nav" :class="{'nav--mobileOpen':header.isMobileActive && mobile}">
        <ul class="menu menu--lvl0" :class="{'menu--fullscreen':mobile }">
          <li
            v-for="link0 in header.linksLvl0"
            :key="link0.name"
            class="menu__item--lvl0"
            :class="{'menu__item--mobile':mobile, 'menu--moveLeftLvl0':isOpenLinkLvl0 && mobile}"
          >
            <a
              v-if="link0.link != ''"
              :to="link0.link"
              class="bSmallText link menu__bSmallText  menu__bSmallText--upper"
              :class="{'menu__bSmallText--mobile':mobile}"
              @click="nav_reset(); openPage(link0.link);"
            >
              {{ link0.name }}
            </a>
            <button
              v-if="link0.link == ''"
              class="bSmallText link menu__bSmallText menu__bSmallText--upper"
              @click="
                resetNavMenus_Lvl1(link0);
                link0.isOpenLinks_Lvl1 = !link0.isOpenLinks_Lvl1;
              "
            >
              {{ link0.name }} >
            </button>
            <ul
              v-if="link0.linkcount > 0 & link0.isOpenLinks_Lvl1"
              class="menu menu--lvl1 menu--dropdown"
            >
              <li
                v-for="link1 in link0.linksLvl1"
                :key="link1.name"
                class="menu__item menu__item--dropdown"
                :class="{'menu--moveLeftLvl1':(isOpenLinkLvl1 && mobile)}"
              >
                <a
                  v-if="link1.link != ''"
                  :to="link1.link"
                  class="bSmallText link menu__bSmallText menu__bSmallText--upper"
                  @click.prevent="
                    openPage(link0.linkParent + link1.link);
                    nav_reset();
                  "
                >
                  {{ link1.name }}
                </a>
                <button
                  v-if="link1.link == ''"
                  class="bSmallText link menu__bSmallText menu__bSmallText--upper "
                  @click="
                    resetNavMenus_Lvl2(link1);
                    link1.isOpenLinks_Lvl2 = !link1.isOpenLinks_Lvl2;
                  "
                >
                  {{ link1.name }} >
                </button>
                <ul
                  v-if="link0.linkcount > 1 & link1.isOpenLinks_Lvl2"
                  class="menu menu--lvl2 menu--dropdown"
                >
                  <li
                    v-for="link2 in link1.linksLvl2"
                    :key="link2.name"
                    class="menu__item menu__item--dropdown"
                  >
                    <a
                      v-if="link2.link != ''"
                      :to="link2.link"
                      class="bSmallText link menu__bSmallText menu__bSmallText--upper"
                      @click.prevent="
                        nav_reset();
                        openPage(
                          link0.linkParent + link1.linkParent + link2.link
                        );
                      "
                    >
                      {{ link2.name }}
                    </a>
                  </li>
                </ul>
              </li>
            </ul>
          </li>
        </ul>
        <button class="bSmallText menu__item menu__item--lvl0 menu__bSmallText--upper" :class="{'menu__item--mobile':mobile}" :href="header.menu.link">
          {{ header.menu.name }}
        </button>
        <button class="bSmallText menu__item menu__item--lvl0  menu__bSmallText--upper" :class="{'menu__bSmallText--lang':mobile}">
          {{ header.lang }}
        </button>
        <a
          class="btnBlue bSmallText menu__item menu__item--lvl0  menu__bSmallText--reg"
          :class="{'menu__item--mobile':mobile}"
        >
          {{ header.registration }}
        </a>
      </div>
      <button v-if="mobile" class="link header__link" :class="{ 'header__link--mobile':mobile}" @click="header.isMobileActive=!header.isMobileActive">
        <svg viewBox="0 0 20 13">
          <path d="M0.605469 11.4805C0.605469 12.0549 1.07109 12.5205 1.64547 12.5205H18.2855C18.8598 12.5205 19.3255 12.0549 19.3255 11.4805C19.3255 10.9062 18.8598 10.4405 18.2855 10.4405H1.64547C1.07109 10.4405 0.605469 10.9062 0.605469 11.4805ZM0.605469 6.28053C0.605469 6.8549 1.07109 7.32053 1.64547 7.32053H18.2855C18.8598 7.32053 19.3255 6.8549 19.3255 6.28053C19.3255 5.70615 18.8598 5.24053 18.2855 5.24053H1.64547C1.07109 5.24053 0.605469 5.70615 0.605469 6.28053ZM1.64547 0.0405273C1.07109 0.0405273 0.605469 0.506151 0.605469 1.08053C0.605469 1.6549 1.07109 2.12053 1.64547 2.12053H18.2855C18.8598 2.12053 19.3255 1.6549 19.3255 1.08053C19.3255 0.506151 18.8598 0.0405273 18.2855 0.0405273H1.64547Z" fill="white" />
        </svg>
      </button>
    </header>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer class="footer">
      <div class="footer__col">
        <div class="footer__logo">
          Logo
        </div>
        <div class="footer__img">
          <v-img
            contain
            :lazy-src="require('~/assets/images/footer/freecassa.png')"
            max-height="60"
            max-width="170"
            :src="require('~/assets/images/footer/freecassa.png')"
            aspect-ratio="1"
            alt=""
          />
        </div>
        <div class="footer__contacts">
          <div class="footer__item">
            <svg v-if="!mobile" class="link" viewBox="0 0 31 30">
              <path
                d="M6.7403 12.6385C9.07656 17.23 12.8405 20.9777 17.432 23.3302L21.0013 19.7609C21.4393 19.3229 22.0883 19.1768 22.6561 19.3715C24.4732 19.9718 26.4363 20.2963 28.4481 20.2963C29.3404 20.2963 30.0705 21.0264 30.0705 21.9187V27.5809C30.0705 28.4732 29.3404 29.2033 28.4481 29.2033C13.2137 29.2033 0.867188 16.8568 0.867188 1.62241C0.867188 0.730083 1.59727 0 2.48959 0H8.16802C9.06034 0 9.79042 0.730083 9.79042 1.62241C9.79042 3.65041 10.1149 5.5973 10.7152 7.4144C10.8937 7.98224 10.7639 8.61498 10.3096 9.06925L6.7403 12.6385Z"
              />
            </svg>
            <a class="bBigText link" :href="footer.contacts[0].link + footer.contacts[0].contact">
              {{ footer.contacts[0].contact }}
            </a>
          </div>
          <div class="footer__item">
            <svg v-if="!mobile" class="link" viewBox="0 0 31 30">
              <path
                fill-rule="evenodd"
                clip-rule="evenodd"
                d="M28.9997 0.945157L29.2593 0.896484C29.7136 0.896484 30.0705 1.25341 30.0705 1.70769V26.2385C30.0705 26.6116 29.8271 26.9037 29.4864 27.0172L20.3361 30.0998L10.6016 26.6927L1.93798 30.0511L1.67839 30.0998C1.22412 30.0998 0.867188 29.7429 0.867188 29.2886V4.75781C0.867188 4.38466 1.11055 4.09263 1.45125 3.97906L10.6016 0.896484L20.3361 4.30354L28.9997 0.945157ZM10.6017 23.4319L20.3361 26.8551V7.56472L10.6017 4.14144V23.4319Z"
              />
            </svg>
            <a class="bBigText link" :href="footer.contacts[1].link + footer.contacts[1].contact">
              {{ footer.contacts[1].contact }}
            </a>
          </div>
          <div class="footer__item">
            <svg v-if="!mobile" class="link" viewBox="0 0 33 27">
              <path
                fill-rule="evenodd"
                clip-rule="evenodd"
                d="M29.2033 0.414062H3.24481C1.46017 0.414062 0.0162241 1.87423 0.0162241 3.65888L0 23.1278C0 24.9124 1.46017 26.3726 3.24481 26.3726H29.2033C30.988 26.3726 32.4481 24.9124 32.4481 23.1278V3.65888C32.4481 1.87423 30.988 0.414062 29.2033 0.414062ZM3.24481 6.90369L16.2241 15.0157L29.2033 6.90369V23.1278H3.24481V6.90369ZM3.24481 3.65888L16.2241 11.7709L29.2033 3.65888H3.24481Z"
              />
            </svg>
            <a class="bBigText link" :href="footer.contacts[2].link + footer.contacts[2].contact">
              {{ footer.contacts[2].contact }}
            </a>
          </div>
        </div>
      </div>
      <div class="footer__col">
        <div class="bSubTitle footer__bSubTitle--upper">
          Меню
        </div>
        <ul class="footer__list">
          <li v-for="link in footer.links" :key="link.name" class="bBigText link">
            <NuxtLink :to="link.link">
              {{ link.name }}
            </NuxtLink>
          </li>
        </ul>
      </div>
      <div class="footer__col">
        <p v-for="text in footer.text" :key="text" class="bBigText">
          {{ text }}
        </p>
      </div>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  // buildModules: ['v-click-outside'],
  name: 'DefaultLayout',
  data () {
    return {
      header: {
        linksLvl0: [
          {
            name: 'Терминал',
            link: 'download',
            linkcount: 0
          },
          {
            name: 'Типы счетов',
            link: 'accountstype',
            linkcount: 0
          },
          {
            name: 'Портфели',
            link: 'portfolio',
            linkcount: 0
          },
          {
            name: 'О нас',
            link: 'aboutUs',
            linkcount: 0
          },
          {
            name: 'Обучение',
            link: '',
            isOpenLinks_Lvl1: false,
            linkParent: 'education',
            linkcount: 2,
            linksLvl1: [
              {
                name: 'Курс',
                link: '',
                linkParent: '/courses',
                isOpenLinks_Lvl2: false,
                linksLvl2: [
                  {
                    name: 'Курс "Начинающим"',
                    link: '/beginner'
                  },
                  {
                    name: 'Курс "Продвинутым"',
                    link: '/advanced'
                  }
                ]
              },
              {
                name: 'Видеоуроки',
                link: '',
                linkParent: '/lessons',
                isOpenLinks_Lvl2: false,
                linksLvl2: [
                  {
                    name: 'Начинающим',
                    link: '/beginner'
                  },
                  {
                    name: 'Продвинутым',
                    link: '/advanced'
                  },
                  {
                    name: 'Криптовалюты',
                    link: '/crypto'
                  }
                ]
              }
            ]
          },
          {
            name: 'Аналитика',
            link: '',
            linkParent: 'analytics',
            isOpenLinks_Lvl1: false,
            linkcount: 2,
            linksLvl1: [
              {
                name: 'Сигналы',
                link: '/signals'
              },
              {
                name: 'Экономический календарь',
                link: '/calendar'
              },
              {
                name: 'Инструменты',
                link: '',
                // linkParent: '/instruments',
                linkParent: '',
                isOpenLinks_Lvl2: false,
                linksLvl2: [
                  {
                    name: 'Аналитические',
                    link: '/analytic'
                  },
                  {
                    name: 'Трейдерские',
                    link: '/trader'
                  },
                  {
                    name: 'Информеры',
                    link: '/informers'
                  },
                  {
                    name: 'Календари',
                    link: '/calendars'
                  }
                ]
              },
              {
                name: 'Публикации',
                link: '',
                linkParent: '/publications',
                isOpenLinks_Lvl2: false,
                linksLvl2: [
                  {
                    name: 'Новости',
                    link: '/news'
                  },
                  {
                    name: 'Технический анализ',
                    link: '/tech'
                  },
                  {
                    name: 'Фундаментальный анализ',
                    link: '/fund'
                  },
                  {
                    name: 'Определение потенциала тренда',
                    link: '/potentional'
                  }
                ]
              }
            ]
          },
          {
            name: 'Контакты',
            link: '/contacts'
          },
          {
            name: 'Документы',
            link: '/documents'
          }
        ],
        menu: {
          name: 'Вход',
          link: ''
        },
        lang: 'RU',
        registration: 'Регистрация',
        isMobileActive: false
      },
      footer: {
        links: [
          {
            name: 'Главная',
            link: '/'
          },
          {
            name: 'Портфели',
            link: '/portfolio'
          },
          {
            name: 'Типы счетов',
            link: '/accountstype'
          },
          {
            name: 'О нас',
            link: '/aboutUs'
          },
          {
            name: 'Контакты',
            link: '/contacts'
          },
          {
            name: 'Документы',
            link: '/documents'
          }
        ],
        text: [
          'Предупреждение:', 'Операции, предлагаемые данным сайтом, могут осуществляться исключительно полностью дееспособными совершеннолетними (достигшими 18 лет) лицами. Операции с финансовыми инструментами, предлагаемые данным сайтом, могут считаться операциями с высоким риском.', 'При совершении таких операций существуют риски частичной либо полной потери денежных средств. Соответственно, настоятельно рекомендуется удерживаться от инвестирования и торговли теми средствами, потерю которых в случае неблагоприятного исхода таких торгов вы не можете себе позволить.', 'Рекомендуем внимательно ознакомиться с нашими Декларацией (Уведомлением) о рисках, Клиентским соглашением и другими регламентирующими документами, прежде чем приступить к совершению операций на данном Веб-сайте.', ' Веб-сайт spacefx.org является собственностью компании PSC TECHNOLOGY DEVELOPMENT CONSULTING S.R.L., Romania, Bucharest Sector 1, Strada Avionului, Nr. 26, Biroul B, floor 1, регистрационный номер 43322212.', 'Компания [company] а, также веб-сайт spacefx.org, не оказывают какие-либо услуг гражданам и жителям США, Бельгии, Турции, Израиля, Сирии, Судана, Ирана, Северной Кореи Японии, а также других стран и юрисдикций, где указанные услуг не могут быть оказаны в силу действующего законодательства.'
        ],
        contacts: [
          {
            link: 'tel:',
            type: 'tel',
            contact: '0321645798021'
          },
          {
            link: 'http://maps.google.com/?q=',
            type: 'map',
            contact: '354 King Street, Melbourne Victoria 5467 Australia'
          },
          {
            link: 'mailto:',
            type: 'mail',
            contact: 'info@mail.com'
          }
        ],
        lang: 'RU',
        registration: 'Регистрация'
      }
    }
  },
  computed: {
    mobile () {
      return this.$vuetify.breakpoint.sm || this.$vuetify.breakpoint.xs
    },
    isOpenLinkLvl0 () {
      let isOpen = false
      this.header.linksLvl0.forEach((element) => {
        if (element.linkcount > 0) {
          if (element.isOpenLinks_Lvl1) {
            isOpen = true
          }
        }
      })
      return isOpen
    },
    isOpenLinkLvl1 () {
      let isOpen = false
      this.header.linksLvl0.forEach((internal) => {
        if (internal.linkcount > 1) {
          internal.linksLvl1.forEach((element) => {
            if (element.isOpenLinks_Lvl2) {
              isOpen = true
            }
          })
        }
      })
      return isOpen
    }
  },
  methods: {
    openPage (link) {
      this.$router.push('/' + link)
    },
    nav_reset () {
      console.log(this.header.isMobileActive)
      this.header.isMobileActive = false
      console.log(this.header.isMobileActive)
      this.header.linksLvl0.forEach((link) => {
        link.isOpenLinks_Lvl1 = false
        if (link.linkcount > 0) {
          link.linksLvl1.forEach((element) => {
            element.isOpenLinks_Lvl2 = false
          })
        }
      })
    },
    resetNavMenus_Lvl1 (value) {
      this.header.linksLvl0.forEach((element) => {
        if (element.name !== value.name) {
          element.isOpenLinks_Lvl1 = false
        }
      })
    },
    resetNavMenus_Lvl2 (value) {
      this.header.linksLvl0.forEach((link) => {
        if (link.linkcount > 0) {
          link.linksLvl1.forEach((element) => {
            if (element.name !== value.name) {
              element.isOpenLinks_Lvl2 = false
            }
          })
        }
      })
    }
  }
}
</script>

<style scoped lang="scss">
@import url("~/assets/scss/abstracts/_variables.scss");
@import url("https://fonts.googleapis.com/css2?family=Manrope:wght@200;300;400;500;600;700;800&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Raleway:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");
.container {
  max-width: 100%;
  width: 100%;
  padding: 0;
  margin: 0;
}
.theme--dark.v-application {
  background: linear-gradient(107.15deg, #1b1b1b 0%, #252c38 100%);
  font-family: "Manrope", sans-serif !important;
  font-size: 16px;
  line-height: 22.5/18 * 1;
  font-weight: normal;
  color: $clr-text-1;
}
.v-application--wrap {
  background: linear-gradient(107.15deg, #1b1b1b 0%, #252c38 100%);
  font-family: "Manrope", sans-serif !important;
  font-weight: normal;

  @include makeitflex(column, flex-start);
  min-height: 100vh;
}
.header {
  @include makeitflex(row, space-between);
  z-index: 1000;
  position: fixed;
  left: 50%;
  top: vwDesk(60);
  transform: translateX(-50%);
  z-index: 1000000;

  align-items: center;
  height: vwDesk(109);
  width: vwDesk(1762);
  border: 1px solid;
  border-radius: vwDesk(25);
  backdrop-filter: blur(5px);
  background: rgba(208, 208, 208, 0.2);
  border-image-source: linear-gradient(180deg, $clr-header-1 0%, $clr-header-2 100%);
  @media (max-width: $w-adapt){
    top: 0;
    left: 0;
    width: 100%;
    height: vhMob(48);
    transform: none;
    background: rgba(208, 208, 208, 0.2);
    backdrop-filter: blur(25px);
    border-radius: 0  0 vwMob(15) vwMob(15)  ;
  }
  &__link{
    display: none;
    &--mobile{
      display: block;
      width: vwMob(20);
      margin-right:vwMob(20) ;
    }
  }
  &__svg {
    width: vwMob(18);
    margin-right: vwDesk(20);
    height: vwDesk(52);
    @media (max-width: $w-adapt){
      height: vwMob(29);
      width: vwMob(50);
      margin-right: vwMob(8);
    }
  }
  &__bSubTitle {
    @include makeitflex(row, flex-start);
    align-items: center;
    height: vwDesk(61);
    padding: vwDesk(37);
    transition: box-shadow $anim-time linear;

    &:hover {
      > svg {
        > circle {
          box-shadow: 0px 4px 20px rgba(19, 155, 253, 0.8);
        }
        > path {
          box-shadow: 0px 4px 20px rgba(19, 155, 253, 0.8);
        }
      }
    }
    &--big{
      text-transform: uppercase;
      font-weight: bold;
      @media(max-width:$w-adapt){
        font-size: $fs-14-m;
        // max-width: vwMob(51);
      }
    }
    @media (max-width: $w-adapt){
      height: vwMob(48);
    }
  }
}
.nav {
    @include makeitflex(row, flex-start);
    align-items: baseline;
    position: relative;
    height: 100%;
    align-items: center;
    transition: transform 4*$anim-time $anim-type;
    @media(max-width:$w-adapt){

      @include makeitflex(column, center);
      height: 100vh - vhMob(48);
      width: 100vw;
      position: absolute;
      top: 0;
      z-index: 100;
      transform: translateY(-100%);
      background: #121721;
    }
    &--mobileOpen{
      transform: translateY(vhMob(48));
    }
}
.menu{
  @include makeitflex(row, flex-start);
  @media(max-width:$w-adapt){
    @include makeitflex(column, flex-start);
  }
  &--lvl0 {
      align-items: center;
  }
  &--lvl1 {
    padding: 1vw !important;
    bottom: 0;
    transform: translate(-10%, 102%);
    white-space: nowrap;
    @media(max-width:$w-adapt){
      padding: none;
      bottom: auto;
      top: 0;
      transform: translate(30vw, -50%);
    }
  }
  &--lvl2 {
    transform: translateX(101%);
    right: 0;
    top: 15%;
    padding: 1vw !important;
    @media(max-width:$w-adapt){
      right: 0;
      padding: none;
      top: 0;
      white-space: normal;
      transform: translateX(5%);
      position: relative !important;
    }
  }
  &--dropdown{
    @include makeitflex(column, flex-start);
    backdrop-filter: blur(5px);
    background: rgba(208, 208, 208, 0.2);
    position: absolute;
    text-align: left;
    border: 1px solid;
    border-radius: vwDesk(25);
    border-image-source: linear-gradient(
      180deg,
      $clr-header-1 0%,
      $clr-header-2 100%
    );
    @media(max-width:$w-adapt){
    backdrop-filter: none;
    // position: relative;
    background: none;
    border: none;
  }
  }
  &--fullscreen{
      z-index: 100;
      @include makeitflex(column, center);
      width: 100vw;
      align-items: center;
    }
  &--moveLeftLvl0{

    transform: translateX(-20vw);
  }
  &--moveLeftLvl1{
    position: relative;
    // transform: translateX(-20vw);
  }
  &__item{
    &--dropdown{
      margin-bottom: 1vw;
      &:last-child {
        margin-bottom: 0;
      }
    }
    &--mobile{
      margin: vhMob(24) 0;
      text-align: center;
      transition: transform 2*$anim_time $anim-type, height 2*$anim_time $anim-type;
    }
    &--lvl0{
      margin-right: vwDesk(40);
    }
  }
  &__bSmallText {
    height: fit-content;
    transition: $anim-time linear;
    text-align: center;
    @media(max-width:$w-adapt){
      margin-right: 0;
    }
    &--upper{
      text-transform: uppercase;
      font-weight: 600;
    }
    &--reg{
      color: $clr-text-1;
      padding: vwDesk(15) vwDesk(35) ;
    }
    &--lang{
      position: absolute;
      top: vhMob(50);
      left: vwMob(25);
    }

  }
}

.footer {
  @include makeitflex(row, space-between);
  margin-top: auto;
  border-radius: vwDesk(40);
  background: linear-gradient(357.58deg, #0f162f -2.27%, #0e141e 93.92%);
  padding: vwDesk(65) vwDesk(45) vwDesk(65) vwDesk(90);
  text-decoration: none;
  color: $clr-text-1;
  align-items: normal;

  backdrop-filter: blur(24px);
  fill: $clr-text-1;

  @media (max-width: $w-adapt){
    padding: vwMob(20) vwMob(30);
    font-size: $fs-14-m;
  }
  &__img{
    @media (max-width:$w-adapt){
      width: vwMob(100);
    }
  }
  &__col {
    @include makeitflex(column, space-between);
    max-width: vwDesk(978);
    @media (max-width: $w-adapt){
      max-width: 100%;
      margin-bottom: vwMob(25) ;
    }
    &:first-child{
      @media (max-width:$w-adapt){
        max-width: 50%;
      }
    }
    > p {
      line-height: 20/16 * 1;
      font-weight: 600;
      @media (max-width: $w-adapt){
        margin-bottom: vwMob(24);
      }
    }
  }
  &__item {
      @include makeitflex(row, flex-start);
      align-items: center;
      margin-top: vwDesk(30);
      transition: fill $anim-time $anim-type, color $anim-time $anim-type;
      &:hover {
        .link{
          color: $clr-btn-1;
          fill: $clr-btn-1;
        }
      }
      @media(max-width:$w-adapt){
        margin-top: vwMob(20);
      }
      > svg {
        margin-right: vwDesk(25);
        width: vwDesk(30);
        fill: $clr-text-1;
      }
    }
  &__contacts {
    @include makeitflex(column, flex-start);
  }
  &__list {
      list-style: disc !important;
      > li {
        margin-top: vwDesk(35);
        @media(max-width:$w-adapt){
          margin-top: vwMob(20);
        }
        > a {
          transition: fill $anim-time linear, color $anim-time linear;
          text-decoration: none;
          color: $clr-text-1;
          &:hover {
            color: $clr-btn-1;
            cursor: pointer;
          }
        }
      }
  }
  &__bSubTitle {
    &--upper{
      text-transform: uppercase;
    }
  }
}
</style>
