<template>
  <div>
    <template v-for="info in pageInfo">
      <div v-if="info.key == $route.params.post" :key="info.key" class="post">
        <div class="head">
          <v-img
            class="pageImgHead"
            :src="require(`~/assets/images/sheets/portfolio/index/${info.imgUrl}`)"
            alt=""
          />
          <div class="head__info">
            <p class="bSubTitle post__bSubTitle--text post__bSubTitle--ttu " :class="{'post__bSubTitle--fs14':mobile}">
              {{ info.headTitle }}
            </p>
            <p class="bTitle head__bTitle head__bTitle--fw" :class="{'head__bTitle--fs12':mobile}">
              {{ info.headPrice }}
            </p>
          </div>
        </div>
        <div class="post__block">
          <p class="bSubTitle post__bSubTitle--text post__bSubTitle--ttu post__bSubTitle--margin" :class="{'post__bSubTitle--fs18':mobile}">
            {{ info.infoTitle }}
          </p>
          <p v-for="text in info.infoText" :key="text" class="bSubTitle post__bSubTitle--text post__bSubTitle--margin">
            {{ text }}
          </p>
        </div>
        <div class="post__prefooter">
          <svg viewBox="0 0 1920 506" class="post__svg">
            <mask
              id="mask0_294_3504"
              style="mask-type:alpha"
              maskUnits="userSpaceOnUse"
              x="0"
              y="0"
              width="1920"
              height="506"
            >
              <rect
                x="1920"
                y="0.000488281"
                width="505.263"
                height="1920"
                transform="rotate(90 1920 0.000488281)"
                fill="#14161B"
              />
            </mask>
            <g mask="url(#mask0_294_3504)">
              <g filter="url(#filter0_f_294_3504)">
                <circle r="1.76188" transform="matrix(-0.995831 -0.0912161 -0.0912161 0.995831 1819.06 281.032)" fill="#00FFA3" />
              </g>
              <g filter="url(#filter1_f_294_3504)">
                <circle r="6.16658" transform="matrix(-0.995831 -0.0912161 -0.0912161 0.995831 958.078 347.585)" fill="#00FFE0" />
              </g>
              <g filter="url(#filter2_f_294_3504)">
                <circle r="4.4047" transform="matrix(-0.995831 -0.0912161 -0.0912161 0.995831 1300.81 256.939)" fill="#00FFE0" />
              </g>
              <g filter="url(#filter3_f_294_3504)">
                <circle r="2.64282" transform="matrix(-0.995831 -0.0912161 -0.0912161 0.995831 1314.86 428.622)" fill="#00FFA3" />
              </g>
              <g filter="url(#filter4_f_294_3504)">
                <circle r="4.61096" transform="matrix(-0.995831 -0.0912161 -0.0912161 0.995831 723.941 408.293)" fill="#00FFA3" />
              </g>
              <g filter="url(#filter5_f_294_3504)">
                <circle r="4.61096" transform="matrix(-0.995831 -0.0912161 -0.0912161 0.995831 240.55 478.02)" fill="#00FFA3" />
              </g>
              <g opacity="0.1" filter="url(#filter6_f_294_3504)">
                <circle r="2.77342" transform="matrix(-0.995831 -0.0912161 -0.0912161 0.995831 135.43 297.112)" fill="#00FFA3" />
              </g>
              <g filter="url(#filter7_f_294_3504)">
                <circle r="2.52632" transform="matrix(-1 -8.74228e-08 -8.74228e-08 1 266.274 365.306)" fill="#00FFA3" />
              </g>
              <g filter="url(#filter8_f_294_3504)">
                <circle r="2.64282" transform="matrix(-0.995831 -0.0912161 -0.0912161 0.995831 487.237 448.833)" fill="#00FFA3" />
              </g>
              <g opacity="0.3" filter="url(#filter9_f_294_3504)">
                <circle r="5.23392" transform="matrix(-0.995831 -0.0912161 -0.0912161 0.995831 786.029 327.784)" fill="#00FFA3" />
              </g>
              <g filter="url(#filter10_f_294_3504)">
                <circle r="16.3027" transform="matrix(-0.995831 -0.0912161 -0.0912161 0.995831 88.3876 445.007)" fill="#00FFA3" />
              </g>
              <g filter="url(#filter11_f_294_3504)">
                <circle r="4.4047" transform="matrix(-0.785176 -0.619273 -0.619273 0.785176 1774.36 458.013)" fill="#00FFA3" />
              </g>
              <g opacity="0.2" filter="url(#filter12_f_294_3504)">
                <circle r="4.4047" transform="matrix(-0.785176 -0.619273 -0.619273 0.785176 1299.42 359.625)" fill="#00FFA3" />
              </g>
              <g opacity="0.5" filter="url(#filter13_f_294_3504)">
                <circle r="4.4047" transform="matrix(-0.785176 -0.619273 -0.619273 0.785176 585.986 471.793)" fill="#00FFA3" />
              </g>
              <g opacity="0.4" filter="url(#filter14_f_294_3504)">
                <circle r="4.09198" transform="matrix(-0.785176 -0.619273 -0.619273 0.785176 221.237 412.611)" fill="#00FFA3" />
              </g>
              <g filter="url(#filter15_f_294_3504)">
                <circle r="9.69034" transform="matrix(-0.785176 -0.619273 -0.619273 0.785176 1700.5 480.538)" fill="#00FFA3" />
              </g>
              <g filter="url(#filter16_f_294_3504)">
                <circle r="35.2376" transform="matrix(-0.995831 -0.0912161 -0.0912161 0.995831 1529.02 485.148)" fill="#00FFA3" />
              </g>
              <g filter="url(#filter17_f_294_3504)">
                <circle r="1.76188" transform="matrix(-0.995831 -0.0912161 -0.0912161 0.995831 1422.73 364.491)" fill="#00FFA3" fill-opacity="0.5" />
              </g>
              <g filter="url(#filter18_f_294_3504)">
                <circle r="1.76188" transform="matrix(-0.995831 -0.0912161 -0.0912161 0.995831 1164.23 448.78)" fill="#00FFA3" fill-opacity="0.5" />
              </g>
              <g filter="url(#filter19_f_294_3504)">
                <circle r="1.76188" transform="matrix(-0.995831 -0.0912161 -0.0912161 0.995831 1225.88 410.38)" fill="#00FFA3" fill-opacity="0.5" />
              </g>
              <g filter="url(#filter20_f_294_3504)">
                <circle r="4.21421" transform="matrix(-0.995831 -0.0912161 -0.0912161 0.995831 1372.63 460.486)" fill="#00FFA3" fill-opacity="0.5" />
              </g>
              <g filter="url(#filter21_f_294_3504)">
                <circle r="4.21421" transform="matrix(-0.995831 -0.0912161 -0.0912161 0.995831 699.759 442.072)" fill="#00FFA3" fill-opacity="0.5" />
              </g>
              <g filter="url(#filter22_f_294_3504)">
                <circle r="4.21421" transform="matrix(-0.995831 -0.0912161 -0.0912161 0.995831 815.97 429.946)" fill="#00FFA3" fill-opacity="0.5" />
              </g>
              <g filter="url(#filter23_f_294_3504)">
                <circle r="4.21421" transform="matrix(-0.995831 -0.0912161 -0.0912161 0.995831 316.771 480.472)" fill="#00FFA3" fill-opacity="0.5" />
              </g>
              <g filter="url(#filter24_f_294_3504)">
                <circle r="4.21421" transform="matrix(-0.995831 -0.0912161 -0.0912161 0.995831 3.5049 489.567)" fill="#00FFA3" fill-opacity="0.5" />
              </g>
              <g filter="url(#filter25_f_294_3504)">
                <circle r="4.21421" transform="matrix(-0.995831 -0.0912161 -0.0912161 0.995831 4.51661 329.904)" fill="#299AC1" />
              </g>
              <g filter="url(#filter26_f_294_3504)">
                <circle r="1.76188" transform="matrix(-0.995831 -0.0912161 -0.0912161 0.995831 1466.74 386.215)" fill="#00FFA3" />
              </g>
              <g filter="url(#filter27_f_294_3504)">
                <path d="M-61.6406 118.232L2014.99 118.232L2014.99 539.622L-61.6406 539.621L-61.6406 118.232Z" fill="url(#paint0_linear_294_3504)" />
              </g>
              <mask
                id="mask1_294_3504"
                style="mask-type:alpha"
                maskUnits="userSpaceOnUse"
                x="0"
                y="276"
                width="1921"
                height="244"
              >
                <rect
                  x="1920"
                  y="519.411"
                  width="1920"
                  height="242.526"
                  transform="rotate(-180 1920 519.411)"
                  fill="#C4C4C4"
                />
              </mask>
              <g mask="url(#mask1_294_3504)">
                <g opacity="0.79" filter="url(#filter28_f_294_3504)">
                  <path d="M876.634 472.422L1993.27 500.211L-55.5764 513.853L876.634 472.422Z" fill="white" />
                </g>
              </g>
            </g>
            <g filter="url(#filter29_f_294_3504)">
              <circle cx="1175.75" cy="355.2" r="3.53684" transform="rotate(-180 1175.75 355.2)" fill="#299AC0" />
            </g>
            <g filter="url(#filter30_f_294_3504)">
              <circle cx="620.968" cy="413.812" r="7.57895" transform="rotate(-180 620.968 413.812)" fill="#299AC0" />
            </g>
            <g filter="url(#filter31_f_294_3504)">
              <circle cx="362.777" cy="412.296" r="13.1368" transform="rotate(-180 362.777 412.296)" fill="#299AC0" />
            </g>
            <g filter="url(#filter32_f_294_3504)">
              <circle
                cx="436.546"
                cy="354.696"
                r="29.3053"
                transform="rotate(-180 436.546 354.696)"
                fill="#299AC0"
                fill-opacity="0.1"
              />
            </g>
            <g filter="url(#filter33_f_294_3504)">
              <circle
                cx="1643.12"
                cy="288"
                r="52.5474"
                transform="rotate(-180 1643.12 288)"
                fill="#299AC0"
                fill-opacity="0.1"
              />
            </g>
            <g filter="url(#filter34_f_294_3504)">
              <circle
                cx="1740.63"
                cy="343.074"
                r="15.6632"
                transform="rotate(-180 1740.63 343.074)"
                fill="#299AC0"
                fill-opacity="0.3"
              />
            </g>
            <g opacity="0.35" filter="url(#filter35_f_294_3504)">
              <circle
                cx="613.391"
                cy="235.453"
                r="17.1789"
                transform="rotate(-180 613.391 235.453)"
                fill="#299AC0"
                fill-opacity="0.1"
              />
            </g>
            <g filter="url(#filter36_f_294_3504)">
              <circle cx="495.665" cy="381.475" r="2.52632" transform="rotate(-180 495.665 381.475)" fill="#299AC0" />
            </g>
            <defs>
              <filter
                id="filter0_f_294_3504"
                x="1815.3"
                y="277.271"
                width="7.52344"
                height="7.52344"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="1" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter1_f_294_3504"
                x="949.91"
                y="339.418"
                width="16.3359"
                height="16.334"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="1" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter2_f_294_3504"
                x="1285.41"
                y="241.534"
                width="30.8086"
                height="30.8101"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="5.5" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter3_f_294_3504"
                x="1310.21"
                y="423.979"
                width="9.28516"
                height="9.28613"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="1" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter4_f_294_3504"
                x="717.328"
                y="401.682"
                width="13.2227"
                height="13.2227"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="1" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter5_f_294_3504"
                x="233.938"
                y="471.408"
                width="13.2227"
                height="13.2227"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="1" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter6_f_294_3504"
                x="130.656"
                y="292.339"
                width="9.54688"
                height="9.54688"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="1" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter7_f_294_3504"
                x="261.75"
                y="360.779"
                width="9.05078"
                height="9.05273"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="1" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter8_f_294_3504"
                x="482.594"
                y="444.19"
                width="9.28516"
                height="9.28613"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="1" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter9_f_294_3504"
                x="778.797"
                y="320.55"
                width="14.4648"
                height="14.4688"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="1" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter10_f_294_3504"
                x="63.082"
                y="419.704"
                width="50.6094"
                height="50.6074"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="4.5" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter11_f_294_3504"
                x="1767.96"
                y="451.608"
                width="12.8086"
                height="12.8096"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="1" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter12_f_294_3504"
                x="1290.01"
                y="350.221"
                width="18.8086"
                height="18.8096"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="2.5" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter13_f_294_3504"
                x="579.582"
                y="465.389"
                width="12.8086"
                height="12.8096"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="1" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter14_f_294_3504"
                x="212.145"
                y="403.52"
                width="18.1836"
                height="18.1846"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="2.5" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter15_f_294_3504"
                x="1688.81"
                y="468.848"
                width="23.3828"
                height="23.3818"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="1" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter16_f_294_3504"
                x="1478.79"
                y="434.908"
                width="100.477"
                height="100.479"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="7.5" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter17_f_294_3504"
                x="1418.97"
                y="360.729"
                width="7.52344"
                height="7.52344"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="1" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter18_f_294_3504"
                x="1160.47"
                y="445.019"
                width="7.52344"
                height="7.52344"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="1" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter19_f_294_3504"
                x="1222.12"
                y="406.618"
                width="7.52344"
                height="7.52344"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="1" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter20_f_294_3504"
                x="1366.41"
                y="454.271"
                width="12.4297"
                height="12.4287"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="1" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter21_f_294_3504"
                x="693.543"
                y="435.857"
                width="12.4297"
                height="12.4287"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="1" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter22_f_294_3504"
                x="809.754"
                y="423.731"
                width="12.4297"
                height="12.4287"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="1" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter23_f_294_3504"
                x="310.555"
                y="474.258"
                width="12.4297"
                height="12.4287"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="1" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter24_f_294_3504"
                x="-2.71094"
                y="483.353"
                width="12.4297"
                height="12.4287"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="1" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter25_f_294_3504"
                x="-1.69922"
                y="323.689"
                width="12.4297"
                height="12.4287"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="1" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter26_f_294_3504"
                x="1463.98"
                y="383.453"
                width="5.52344"
                height="5.52344"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="0.5" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter27_f_294_3504"
                x="-125.641"
                y="54.2319"
                width="2204.63"
                height="549.39"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="32" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter28_f_294_3504"
                x="-83.5781"
                y="444.422"
                width="2104.84"
                height="97.4316"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="14" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter29_f_294_3504"
                x="1170.21"
                y="349.664"
                width="11.0742"
                height="11.0732"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="1" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter30_f_294_3504"
                x="605.391"
                y="398.232"
                width="31.1562"
                height="31.1582"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="4" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter31_f_294_3504"
                x="345.641"
                y="395.159"
                width="34.2734"
                height="34.2734"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="2" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter32_f_294_3504"
                x="394.242"
                y="312.391"
                width="84.6094"
                height="84.6104"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="6.5" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter33_f_294_3504"
                x="1577.57"
                y="222.453"
                width="131.094"
                height="131.095"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="6.5" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter34_f_294_3504"
                x="1711.96"
                y="314.411"
                width="57.3281"
                height="57.3262"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="6.5" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter35_f_294_3504"
                x="583.211"
                y="205.274"
                width="60.3594"
                height="60.3579"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="6.5" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <filter
                id="filter36_f_294_3504"
                x="491.141"
                y="376.948"
                width="9.05078"
                height="9.05273"
                filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB"
              >
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                <feGaussianBlur stdDeviation="1" result="effect1_foregroundBlur_294_3504" />
              </filter>
              <linearGradient
                id="paint0_linear_294_3504"
                x1="99.4951"
                y1="-196.303"
                x2="124.028"
                y2="591.073"
                gradientUnits="userSpaceOnUse"
              >
                <stop offset="0.137331" stop-color="#161920" stop-opacity="0" />
                <stop offset="0.441658" stop-color="#1E232E" stop-opacity="0.58" />
                <stop offset="0.616248" stop-color="#22356F" stop-opacity="0.6" />
                <stop offset="0.765625" stop-color="#1097BB" stop-opacity="0.68" />
                <stop offset="1" stop-color="#00FFE0" />
              </linearGradient>
            </defs>
          </svg>
          <button class="btnBlue post__btnBlue ">
            {{ btnText }}
          </button>
        </div>
      </div>
    </template>
  </div>
</template>

<script>
export default {
  name: 'PortfolisssPage',
  // async asyncData ({ params }) {
  //   const post = params.post // When calling /abc the slug will be "abc"
  //   return { post }
  // },
  data () {
    return {
      btnText: 'Подать заявку',
      pageInfo:
      [
        {
          key: 'pharmaceut',
          headTitle: 'Инвестирование в фармацевтику',
          imgUrl: 'preview1.png',
          headPrice: 'от $100, 000',
          infoTitle: 'Доходность этого портфеля составляет от 7-12% при условии инвестирования от 1 года.',
          infoText: [
            'Долгосрочный вариант инвестирования, с чуть выше минимальной степенью риска. Отличается постоянной стабильностью, и показывает хорошие результаты в перспективе от 2 лет. Подойдет для сильных инвесторов, которые работают на перспективу. Работа фонда в этом сегменте складывается таким образом- наши эксперты ведут работу с прямыми инвестициями в акции фармацевтических компаний США.',
            'Американский фармсегмент довольно стабилен, и чаще всего происходит так что он превосходит ожидания аналитиков. Акции растут в цене, а спрос на препараты постоянно растет, ведь население стареет. За счет этого в ближайшие пять лет эта сфера будет в стадии уверенного и стабильного роста, что позволит нашим инвестором получать свой ежегодный процент не изучая сферу фармацевтики и ее рынок.'
          ]
        },
        {
          key: 'realty',
          headTitle: 'Инвестирование в фармацевтику',
          imgUrl: 'preview2.png',
          headPrice: 'от $100, 000',
          infoTitle: 'Доходность этого портфеля составляет от 7-12% при условии инвестирования от 1 года.',
          infoText: [
            'Долгосрочный вариант инвестирования, с чуть выше минимальной степенью риска. Отличается постоянной стабильностью, и показывает хорошие результаты в перспективе от 2 лет. Подойдет для сильных инвесторов, которые работают на перспективу. Работа фонда в этом сегменте складывается таким образом- наши эксперты ведут работу с прямыми инвестициями в акции фармацевтических компаний США.',
            'Американский фармсегмент довольно стабилен, и чаще всего происходит так что он превосходит ожидания аналитиков. Акции растут в цене, а спрос на препараты постоянно растет, ведь население стареет. За счет этого в ближайшие пять лет эта сфера будет в стадии уверенного и стабильного роста, что позволит нашим инвестором получать свой ежегодный процент не изучая сферу фармацевтики и ее рынок.'
          ]
        },
        {
          key: 'it',
          headTitle: 'Инвестирование в фармацевтику',
          imgUrl: 'preview3.png',
          headPrice: 'от $100, 000',
          infoTitle: 'Доходность этого портфеля составляет от 7-12% при условии инвестирования от 1 года.',
          infoText: [
            'Долгосрочный вариант инвестирования, с чуть выше минимальной степенью риска. Отличается постоянной стабильностью, и показывает хорошие результаты в перспективе от 2 лет. Подойдет для сильных инвесторов, которые работают на перспективу. Работа фонда в этом сегменте складывается таким образом- наши эксперты ведут работу с прямыми инвестициями в акции фармацевтических компаний США.',
            'Американский фармсегмент довольно стабилен, и чаще всего происходит так что он превосходит ожидания аналитиков. Акции растут в цене, а спрос на препараты постоянно растет, ведь население стареет. За счет этого в ближайшие пять лет эта сфера будет в стадии уверенного и стабильного роста, что позволит нашим инвестором получать свой ежегодный процент не изучая сферу фармацевтики и ее рынок.'
          ]
        },
        {
          key: 'crypto',
          headTitle: 'Инвестирование в фармацевтику',
          imgUrl: 'preview4.png',
          headPrice: 'от $100, 000',
          infoTitle: 'Доходность этого портфеля составляет от 7-12% при условии инвестирования от 1 года.',
          infoText: [
            'Долгосрочный вариант инвестирования, с чуть выше минимальной степенью риска. Отличается постоянной стабильностью, и показывает хорошие результаты в перспективе от 2 лет. Подойдет для сильных инвесторов, которые работают на перспективу. Работа фонда в этом сегменте складывается таким образом- наши эксперты ведут работу с прямыми инвестициями в акции фармацевтических компаний США.',
            'Американский фармсегмент довольно стабилен, и чаще всего происходит так что он превосходит ожидания аналитиков. Акции растут в цене, а спрос на препараты постоянно растет, ведь население стареет. За счет этого в ближайшие пять лет эта сфера будет в стадии уверенного и стабильного роста, что позволит нашим инвестором получать свой ежегодный процент не изучая сферу фармацевтики и ее рынок.'
          ]
        }
      ],
      textblock:
      [
        'Самый доходный портфель для инвестирования со средним риском. Подойдет тем инвесторам, которые готовы идти на определенные риски для получения большей прибыли. В данном направлении работа фонда разделяется на несколько подходов. Первый - это закупка различных криптовалютных активов на споте при минимальной цене, их холд (хранение) и их дальнейшая перепродажа на пиках роста активов. ',
        'Второй - это ведение активной торговли управляющих счетами фонда исключительно криптовалютными активами и получение заработка на разнице цен CFD. Это также называется краткосрочной торговлей, спекулятивной, агрессивной и т.д. Как правило, сделки краткосрочные  - от нескольких минут, до нескольких часов.  Прибыльность таких сделок может варьироваться от 37% и достигать 136% в зависимости от торгуемого объема. Такие цифры достигаются благодаря достаточно высокой волатильности крипторынка. '
      ]
    }
  },
  computed: {
    mobile () {
      return this.$vuetify.breakpoint.sm || this.$vuetify.breakpoint.xs
    }
  }
}

</script>
<style lang="scss" scoped>
.post{
  .head{
    position: relative;
    width: 100%;
    margin-bottom: vwDesk(120);
    @media(max-width:$w-adapt){
      margin-bottom: vwMob(20);
    }
    &__info{
      position: absolute;
      left: vwDesk(80);
      bottom: vwDesk(40);
      background: #171B21;
      box-shadow: inset 0px 0px 24px #000000;
      border-radius: vwDesk(20);
      padding: vwDesk(30) vwDesk(35);
      max-width: vwDesk(300);
      @media(max-width:$w-adapt){
        max-width: vwMob(170);
        border-radius: vwMob(10);
        left: vwMob(40);
        bottom: vwMob(15);

      }
    }
    &__bTitle{
      margin-top: vwDesk(15);
      @media(max-width:$w-adapt){
        margin-top: vwMob(10);
      }
      &--fw{
        font-weight: 400;
      }
      &--fs12{
        font-size: $fs-12-m;
      }
    }
  }
  &__bSubTitle{
    &--text{
      line-height: 33/24*1;
      font-weight: normal;
    }
    &--ttu{
      font-weight: 800;
      text-transform: uppercase;
    }
    &--margin{
      margin-bottom: $fs-36;
      @media(max-width:$w-adapt){
        margin-bottom: vwMob(20);
      }
    }
    &--fs14{
      font-size: $fs-14-m;
    }
    &--fs18{
      font-size: $fs-18-m;
    }
  }
  &__block{
    padding: 0 vwDesk(120);
    @media(max-width:$w-adapt){
      padding: 0 vwMob(25);

    }
  }
  &__prefooter{
    margin: -2vw 0;
    position: relative;
    @media(max-width:$w-adapt){
      height: vwMob(320);
    }
  }
  &__btnBlue{
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    padding: vwDesk(15) vwDesk(48);
    white-space: nowrap;
    @media(max-width:$w-adapt){
      padding: vwMob(15) vwMob(48);
    }
  }
  &__svg{
    @media(max-width:$w-adapt){
      height: 100%;
    }
  }
}
</style>
