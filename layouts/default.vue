<template>
  <v-app>
    <header v-click-outside="nav_reset" class="header">
      <NuxtLink class="header_logo" to="/" @click="nav_reset">
        <svg viewBox="0 0 89 52">
          <circle cx="26" cy="26" r="26" />
          <path
            d="M63 2.6782e-06C69.8956 2.37678e-06 76.5088 2.73928 81.3848 7.61522C86.2607 12.4912 89 19.1044 89 26C89 32.8956 86.2607 39.5088 81.3848 44.3848C76.5088 49.2607 69.8956 52 63 52L63 26L63 2.6782e-06Z"
          />
        </svg>
        <p>Lorem ipsum</p>
      </NuxtLink>
      <div class="header_nav">
        <ul class="header_nav_lvl0">
          <li v-for="link0 in header.linksLvl0" :key="link0.name">
            <NuxtLink
              v-if="link0.link !=''"
              :to="link0.link"
              class="btn_nav transparent"
              @click="nav_reset"
            >
              {{ link0.name }}
            </NuxtLink>
            <button
              v-if="link0.link ==''"
              class="btn_nav transparent link_lvl0"
              @click="navLvl0_click(link0); link0.linksLvl1IsOpen = !link0.linksLvl1IsOpen"
            >
              {{ link0.name }} >
              <!-- @click="navLvl0_click(link0.linksLvl1IsOpen)" -->
            </button>
            <ul v-if="link0.linkcount >0" class="header_nav_lvl1" :class="{ visible:link0.linksLvl1IsOpen }">
              <li v-for="link1 in link0.linksLvl1" :key="link1.name" class="link">
                <a
                  v-if="link1.link !=''"
                  :to="link1.link"
                  class="btn_nav  link_lvl1"
                  @click.prevent="openPage(link0.linkParent + link1.link); nav_reset()"
                >
                  {{ link1.name }}
                </a>
                <button
                  v-if="link1.link ==''"
                  class="btn_nav transparent link_lvl1"
                  @click="navLvl1_click(link1); link1.linksLvl2IsOpen=!link1.linksLvl2IsOpen"
                >
                  {{ link1.name }} >
                </button>
                <ul v-if="link0.linkcount>1" class="header_nav_lvl2" :class="{ visible:link1.linksLvl2IsOpen }">
                  <li v-for="link2 in link1.linksLvl2" :key="link2.name" class="link">
                    <a
                      v-if="link2.link !=''"
                      :to="link2.link"
                      class="btn_nav  link_lvl2"
                      @click.prevent="openPage(link0.linkParent + link1.linkParent + link2.link); nav_reset()"
                    >
                      {{ link2.name }}
                    </a>
                  </li>
                </ul>
              </li>
            </ul>
          </li>
        </ul>
        <button class="btn_nav transparent">
          {{ header.lang }}
        </button>
        <a class="btn_nav btn_blue btn_reg">
          {{ header.registration }}
        </a>
      </div>
    </header>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer class="footer">
      <div class="footer_col">
        <div class="footer_logo">
          Logo
        </div>
        <div class="footer_img">
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
        <div class="footer_contacts">
          <div class="footer_contacts_item">
            <svg viewBox="0 0 31 30">
              <path
                d="M6.7403 12.6385C9.07656 17.23 12.8405 20.9777 17.432 23.3302L21.0013 19.7609C21.4393 19.3229 22.0883 19.1768 22.6561 19.3715C24.4732 19.9718 26.4363 20.2963 28.4481 20.2963C29.3404 20.2963 30.0705 21.0264 30.0705 21.9187V27.5809C30.0705 28.4732 29.3404 29.2033 28.4481 29.2033C13.2137 29.2033 0.867188 16.8568 0.867188 1.62241C0.867188 0.730083 1.59727 0 2.48959 0H8.16802C9.06034 0 9.79042 0.730083 9.79042 1.62241C9.79042 3.65041 10.1149 5.5973 10.7152 7.4144C10.8937 7.98224 10.7639 8.61498 10.3096 9.06925L6.7403 12.6385Z"
              />
            </svg>
            <a href="">(0321) 645-798-021</a>
          </div>
          <div class="footer_contacts_item">
            <svg viewBox="0 0 31 30">
              <path
                fill-rule="evenodd"
                clip-rule="evenodd"
                d="M28.9997 0.945157L29.2593 0.896484C29.7136 0.896484 30.0705 1.25341 30.0705 1.70769V26.2385C30.0705 26.6116 29.8271 26.9037 29.4864 27.0172L20.3361 30.0998L10.6016 26.6927L1.93798 30.0511L1.67839 30.0998C1.22412 30.0998 0.867188 29.7429 0.867188 29.2886V4.75781C0.867188 4.38466 1.11055 4.09263 1.45125 3.97906L10.6016 0.896484L20.3361 4.30354L28.9997 0.945157ZM10.6017 23.4319L20.3361 26.8551V7.56472L10.6017 4.14144V23.4319Z"
              />
            </svg>
            <a href="">354 King Street, Melbourne Victoria 5467 Australia</a>
          </div>
          <div class="footer_contacts_item">
            <svg viewBox="0 0 33 27">
              <path
                fill-rule="evenodd"
                clip-rule="evenodd"
                d="M29.2033 0.414062H3.24481C1.46017 0.414062 0.0162241 1.87423 0.0162241 3.65888L0 23.1278C0 24.9124 1.46017 26.3726 3.24481 26.3726H29.2033C30.988 26.3726 32.4481 24.9124 32.4481 23.1278V3.65888C32.4481 1.87423 30.988 0.414062 29.2033 0.414062ZM3.24481 6.90369L16.2241 15.0157L29.2033 6.90369V23.1278H3.24481V6.90369ZM3.24481 3.65888L16.2241 11.7709L29.2033 3.65888H3.24481Z"
              />
            </svg>
            <a href="">info@mail.com</a>
          </div>
        </div>
      </div>
      <div class="footer_col">
        <div class="footer_menu">
          Меню
        </div>
        <ul class="footer_menu_list">
          <li v-for="link in footer.links" :key="link.name">
            <NuxtLink :to="link.link">
              {{ link.name }}
            </NuxtLink>
          </li>
        </ul>
      </div>
      <div class="footer_col">
        <p>Предупреждение:</p>
        <p>
          Операции, предлагаемые данным сайтом, могут осуществляться
          исключительно полностью дееспособными совершеннолетними (достигшими
          18 лет) лицами. Операции с финансовыми инструментами, предлагаемые
          данным сайтом, могут считаться операциями с высоким риском.
        </p>
        <p>
          При совершении таких операций существуют риски частичной либо полной
          потери денежных средств. Соответственно, настоятельно рекомендуется
          удерживаться от инвестирования и торговли теми средствами, потерю
          которых в случае неблагоприятного исхода таких торгов вы не можете
          себе позволить.
        </p>
        <p>
          Рекомендуем внимательно ознакомиться с нашими Декларацией
          (Уведомлением) о рисках, Клиентским соглашением и другими
          регламентирующими документами, прежде чем приступить к совершению
          операций на данном Веб-сайте.
        </p>
        <p>
          Веб-сайт spacefx.org является собственностью компании PSC TECHNOLOGY
          DEVELOPMENT CONSULTING S.R.L., Romania, Bucharest Sector 1, Strada
          Avionului, Nr. 26, Biroul B, floor 1, регистрационный номер
          43322212.
        </p>
        <p>
          Компания [company] а, также веб-сайт spacefx.org, не оказывают
          какие-либо услуг гражданам и жителям США, Бельгии, Турции, Израиля,
          Сирии, Судана, Ирана, Северной Кореи Японии, а также других стран и
          юрисдикций, где указанные услуг не могут быть оказаны в силу
          действующего законодательства.
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
      clipped: false,
      drawer: false,
      fixed: false,
      header: {
        linksLvl0: [
          {
            name: 'Терминал',
            link: '/download',
            linkcount: 0
          },
          {
            name: 'Типы счетов',
            link: '/accountstype',
            linkcount: 0
          },
          {
            name: 'Портфели',
            link: '/portfolio',
            linkcount: 0
          },
          {
            name: 'О нас',
            link: '/aboutUs',
            linkcount: 0
          },
          {
            name: 'Обучение',
            link: '',
            linksLvl1IsOpen: false,
            linkParent: 'education',
            linkcount: 2,
            linksLvl1:
            [
              {
                name: 'Курс',
                link: '',
                linkParent: '/courses',
                linksLvl2IsOpen: false,
                linksLvl2:
                [
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
                linksLvl2IsOpen: false,
                linksLvl2:
                [
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
            linksLvl1IsOpen: false,
            linkcount: 2,
            linksLvl1:
            [
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
                linksLvl2IsOpen: false,
                linksLvl2:
                [
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
                linksLvl2IsOpen: false,
                linksLvl2:
                [
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
          },
          {
            name: 'Вход',
            link: ''
          }
        ],
        lang: 'RU',
        registration: 'Регистрация'
      },
      footer: {
        links: [
          {
            name: 'Главная',
            link: '/'
          },
          {
            name: 'Аналитика',
            link: ''
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
        lang: 'RU',
        registration: 'Регистрация'
      },
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  },
  methods: {
    openPage (link) {
      this.$router.push('/' + link)
    },
    nav_reset () {
      this.header.linksLvl0.forEach((link) => {
        link.linksLvl1IsOpen = false
        if (link.linkcount > 0) {
          link.linksLvl1.forEach((element) => {
            element.linksLvl2IsOpen = false
          })
        }
      })
    },
    navLvl0_click (value) {
      this.header.linksLvl0.forEach((element) => {
        if (element.name !== value.name) {
          element.linksLvl1IsOpen = false
        }
      })
    },
    navLvl1_click (value) {
      this.header.linksLvl0.forEach((link) => {
        if (link.linkcount > 0) {
          link.linksLvl1.forEach((element) => {
            if (element.name !== value.name) {
              element.linksLvl2IsOpen = false
            }
          })
        }
      })
      // value = !value
    }
  }
}
</script>

<style scoped lang='scss'>
@import url('~/assets/scss/abstracts/_variables.scss');
@import url('https://fonts.googleapis.com/css2?family=Manrope:wght@200;300;400;500;600;700;800&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Raleway:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
.container{
  max-width: 100%;
  width: 100%;
  padding: 0;
  margin: 0;
}
.theme--dark.v-application{
  background: linear-gradient(107.15deg, #1B1B1B 0%, #252C38 100%);
  font-family: 'Manrope', sans-serif;
  font-size: 16px;
  line-height: 22.5/18*1;
  font-weight: normal;
  color: $textColor1;
}
.v-application--wrap{

  background: linear-gradient(107.15deg, #1B1B1B 0%, #252C38 100%);
  font-family: 'Manrope', sans-serif;
  font-weight: normal;

  @include makeitflex(column, flex-start);
  min-height: 100vh;
}
.header {
  @include makeitflex(row, space-between);
  z-index: 1000;
  position: fixed;
  left: 50%;
  transform: translate(-50%, 60px);
  z-index: 1000000;

  align-items: center;
  height: 109/1920*100vw;
  width: 1762/1920*100%;
  border: 1px solid;
  border-radius: 25px;
  backdrop-filter: blur(5px);
  background: rgba(208, 208, 208, 0.2);
  border-image-source: linear-gradient(180deg, #6A6868 0%, rgba(26, 32, 44, 0) 100%);
  &_logo {
    @include makeitflex(row, flex-start);
    align-items: center;
    height: 61px;
    padding: 37px;
    text-decoration: none;
    text-transform: uppercase;
    font-style: normal;
    font-family: 'Manrope', sans-serif;
    font-size: $h5FS;
    font-weight: bold;
    color: #E2E3E3;
    cursor: pointer;
    transition: fill $transition_time linear, box-shadow $transition_time linear, color $transition_time linear;
    fill:#E2E3E3;
    &:hover{
      color: #1CB0FF;
      cursor: pointer;
      fill: #1CB0FF;
      >svg{
        >circle{
          box-shadow: 0px 4px 20px rgba(19, 155, 253, 0.8);
        }
        >path{
          box-shadow: 0px 4px 20px rgba(19, 155, 253, 0.8);
        }
      }
    }
    >svg{
      margin-right: 20px;
      height: 52/1920*100vw;
    }
    >p{
      cursor: pointer;
    }
  }
  &_nav{
    @include makeitflex(row, flex-start);
      align-items: center;
    &_lvl0{
      align-items: center;
      @include makeitflex(row, flex-start);
    }
    &_lvl1{
      backdrop-filter: blur(5px);
      background: rgba(208, 208, 208, 0.2);
      position: absolute;
      bottom: 0;
      transform: translate(-10%,101%);
      text-align: left;
      display: none;
      border: 1px solid;
      border-radius: 25px;
      padding: 1vw !important;
      border-image-source: linear-gradient(180deg, #6A6868 0%, rgba(26, 32, 44, 0) 100%);

    }
    &_lvl2{
      position: absolute;
      right: 0;
      top: 50%;
      transform: translate(111%,-15%);
      text-align: left;
      width: auto;
      display: none;
      border: 1px solid;
      border-radius: 25px;
      padding: 1vw !important;
      backdrop-filter: blur(5px);
      background: rgba(208, 208, 208, 0.2);
      border-image-source: linear-gradient(180deg, #6A6868 0%, rgba(26, 32, 44, 0) 100%);
    }
  }
  .link{
    margin-bottom: 1vw;
    position: relative;
    &:last-child{
      margin-bottom: 0;
    }
    &_lvl0{
      position: relative;
    }
    &_lvl1{
      position: relative;
      margin-left: 0;
      white-space: nowrap;
      width: 100%;
      text-align: left;
    }
    &_lvl2{
      text-align: left;
      width: 100%;
      margin-left: 0;
    }
  }

}
.visible{
  display: block;
}
.footer {
    @include makeitflex(row, space-between);
    margin-top: auto;
    border-radius: 40px;
    background: linear-gradient(357.58deg, #0F162F -2.27%, #0E141E 93.92%);
    padding: 65/1920*100vw 45/1920*100vw 65/1920*100vw 90/1920*100vw;
    text-decoration: none;
    font-family: 'Manrope', sans-serif !important;
    font-size: $h7FS;
    font-weight: 600;
    color: $textColor1;
    align-items: normal;

    backdrop-filter: blur(24px);
    fill:$textColor1;
    &_col{
        @include makeitflex(column, space-between);
        max-width: 978/1920*100vw;
        >p{
        letter-spacing: 0px;
        line-height: 20/16*1;
        font-weight: 600;

        }
    }
    &_contacts{
        @include makeitflex(column,flex-start);
        &_item{

            @include makeitflex(row,flex-start);
            align-items: center;
            margin-top: 30px;
            transition: fill $transition_time linear, color $transition_time linear;
            >svg{
                margin-right: 25px;
                width: 30px;
                fill: $textColor1;
            }
            >a{

                text-decoration: none;
                color: $textColor1;
            }
            &:hover{
                >svg,>a{
                    color: #1CB0FF;
                    fill: #1CB0FF;
                }
            }
        }
    }
    &_menu{
      text-transform: uppercase;
      font-size: $h5FS;
      font-weight: 700;
      &_list{
        list-style: disc !important;
        >li{
          margin-top: 35px;
          >a{
            transition: fill $transition_time linear, color $transition_time linear;
            text-decoration: none;
            color: $textColor1;
            &:hover{
                color: #1CB0FF;
                cursor: pointer;
            }
          }
        }
      }
    }
}

</style>
