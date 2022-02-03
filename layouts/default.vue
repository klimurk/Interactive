<template>
  <v-app>
    <header class="header">
      <NuxtLink class="header_logo" to="/">
        <svg viewBox="0 0 89 52">
          <circle cx="26" cy="26" r="26" />
          <path
            d="M63 2.6782e-06C69.8956 2.37678e-06 76.5088 2.73928 81.3848 7.61522C86.2607 12.4912 89 19.1044 89 26C89 32.8956 86.2607 39.5088 81.3848 44.3848C76.5088 49.2607 69.8956 52 63 52L63 26L63 2.6782e-06Z"
          />
        </svg>
        <p>Lorem ipsum</p>
      </NuxtLink>
      <div class="header_nav">
        <NuxtLink
          v-for="link in header.links"
          :key="link.link"
          :to="link.link"
          class="btn_nav transparent"
        >
          {{ link.name }}
        </NuxtLink>
        <!-- <NuxtLink to="/" class="btn_nav transparent" />
        <NuxtLink to="/" class="btn_nav transparent" />
        <NuxtLink to="/" class="btn_nav transparent" />
        <NuxtLink to="/" class="btn_nav transparent" />
        <NuxtLink to="/" class="btn_nav transparent" />
        <NuxtLink to="/" class="btn_nav transparent" />
        <NuxtLink to="/" class="btn_nav transparent" /> -->
        <button to="/" class="btn_nav transparent">
          {{ header.lang }}
        </button>
        <a class="btn_nav btn_blue btn_reg">
          {{ header.registration }}
        </a>
      </div>
    </header>
    <!-- nav left -->
    <!-- <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer> -->
    <!-- ---------------------------- -->
    <!-- <v-app-bar color="#" fixed app>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-btn icon @click.stop="miniVariant = !miniVariant">
        <v-icon>mdi-{{ `chevron-${miniVariant ? "right" : "left"}` }}</v-icon>
      </v-btn>
      <v-btn icon @click.stop="clipped = !clipped">
        <v-icon>mdi-application</v-icon>
      </v-btn>
      <v-btn icon @click.stop="fixed = !fixed">
        <v-icon>mdi-minus</v-icon>
      </v-btn>
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <v-btn icon @click.stop="rightDrawer = !rightDrawer">
        <v-icon>mdi-menu</v-icon>
      </v-btn>
    </v-app-bar> -->
    <!-- ================================= -->
    <!-- main part ======================= -->
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <!-- ==================================  -->
    <!-- rigth nav -->
    <!-- <v-navigation-drawer v-model="rightDrawer" :right="right" temporary fixed>
      <v-list>
        <v-list-item @click.native="right = !right">
          <v-list-item-action>
            <v-icon light> mdi-repeat </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer (click me)</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer> -->
    <!-- footer  -->
    <!-- <v-footer :absolute="!fixed" app> -->
    <div class="footer">
      <div class="footer_col">
        <div class="footer_logo">
          Logo
        </div>
        <div class="footer_img">
          <v-img
            contain
            lazy-src="/assets/images/footer/freecassa.png"
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
          <li><a href="">Главная</a></li>
          <li><a href="">Аналитика</a></li>
          <li><a href="">Типы счетов</a></li>
          <li><a href="">О нас</a></li>
          <li><a href="">Контакты</a></li>
          <li><a href="">Документация</a></li>
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
    </div>
    <!-- </v-footer> -->
    <!-- left nav -->
    <!-- ------- -->
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      header: {
        links: [
          {
            name: 'Типы счетов',
            link: 'accountstype'
          },
          {
            name: 'Портфели',
            link: ''
          },
          {
            name:
            'О нас',
            link: ''
          },
          {
            name:
            'Обучение',
            link: ''
          },
          {
            name:
            'Аналитика',
            link: ''
          },
          {
            name:
            'Контакты',
            link: ''
          },
          {
            name:
            'Документы',
            link: ''
          },
          {
            name:
            'Вход',
            link: ''
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
  }
}
</script>

<style scoped lang='scss'>
@import url('~/assets/scss/abstracts/_placeholders.scss');
@import url('~/assets/scss/abstracts/_variables.scss');
.container{
  max-width: 100%;
    width: 100%;
    padding: 0;
    margin: 0;
}
.theme--dark.v-application{
  //  background:linear-gradient(135deg, $backgroundColor1, $backgroundColor2);
    background: linear-gradient(107.15deg, #1B1B1B 0%, #252C38 100%);
    font-family: 'Manrope', sans-serif;
    font-size: 16px;
    line-height: 22.5/18*100%;
    font-weight: normal;
    color: $textColor1;
}
.v-application--wrap{

    // background:linear-gradient(135deg, $backgroundColor1, $backgroundColor2);
    background: linear-gradient(107.15deg, #1B1B1B 0%, #252C38 100%);
    font-family: 'Manrope', sans-serif;
    font-weight: normal;

    @include makeitflex(column, flex-start);
    min-height: 100vh;
}
@import url('~/assets/scss/layout/_header.scss');
@import url('~/assets/scss/layout/_footer.scss');

</style>
