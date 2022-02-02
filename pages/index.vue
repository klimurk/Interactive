<template>
  <div>
    <div class="mainPage">
      <div class="mainPage_block1">
        <video autoplay playsinline muted loop poster="~/assets/images/temp/mainBlock1.png">
          <source src="~/assets/video/main/block1.mp4" type="video/mp4">
        </video>
        <div class="mainPage_block1_description">
          <p class="title">
            {{ datablock1.title }}
          </p>
          <br>
          <p>
            {{ datablock1.text }}
          </p>
          <br>
          <a href="">
            {{ datablock1.btn_text }}
          </a>
        </div>
      </div>
      <div class="mainPage_block2">
        <div>
          <p class="title">
            {{ datablock1.title }}
          </p>
          <p class="text">
            {{ datablock1.text }}
          </p>
        </div>
        <v-img lazy-src="/assets/images/temp/mainBlock2.png" :src="require('~/assets/images/temp/mainBlock2.png')" alt="" />
      </div>
      <div class="mainPage_block3">
        <div class="mainPage_block3_col wide">
          <div class="mainPage_block3_item dataBlock3_b1">
            <p class="title">
              {{ datablock3.items[0].title }}
            </p>
            <p class="text">
              {{ datablock3.items[0].text }}
            </p>
          </div>
          <div class="mainPage_block3_item dataBlock3_b2">
            <p class="title">
              {{ datablock3.items[1].title }}
            </p>
            <p class="text">
              {{ datablock3.items[1].text }}
            </p>
          </div>
        </div>
        <div class="mainPage_block3_col middle" />
        <div class="mainPage_block3_col tall">
          <div class="mainPage_block3_item dataBlock3_b3">
            <p class="title">
              {{ datablock3.items[2].title }}
            </p>
            <p class="text">
              {{ datablock3.items[2].text }}
            </p>
          </div>
          <div class="mainPage_block3_item dataBlock3_b4">
            <p class="title">
              {{ datablock3.items[3].title }}
            </p>
            <p class="text">
              {{ datablock3.items[3].text }}
            </p>
          </div>
        </div>
      </div>
      <div
        id="block4"
        class="mainPage_block4"
        :class="{ afterEnable: datablock4.isAfterEnable }"
      >
        <div v-for="item in datablock4.items" :key="item.id" class="mainPage_block4_item">
          <p class="title" @click="setCount(item.id)">
            {{ item.hasOwnProperty('symbol')? item.symbol:'' }}
            {{ item.count | addComma }}
          </p>
          <p class="text">
            {{ item.text }}
          </p>
        </div>
      </div>
      <div class="mainPage_block5">
        <p class="text">
          {{ datablock5.head_text.line1 }}
        </p>
        <p class="title">
          {{ datablock5.head_text.line2 }}
        </p>
        <div class="mainPage_block5_anim">
          <div
            v-for="item in datablock5.squares"
            :key="item.id"
            class="mainPage_block5_anim_square"
            :class="{
              s1: item.id==0,
              s2: item.id==1,
              s3: item.id==2,
            }"
            @click="block5Rotate"
          >
            <!-- <svg viewBox="0 0 240 241">
              <g id="Group 2412">
                <g id="Group 2465">
                  <g id="Rectangle 1153" filter="url(#filter0_di_167_1206)">
                    <rect
                      x="209"
                      y="32"
                      width="178"
                      height="178"
                      transform="rotate(90 209 32)"
                      fill="#0D0F13"
                    />
                  </g>
                  <rect
                    id="Rectangle 1156"
                    x="198"
                    y="47"
                    width="150"
                    height="155"
                    transform="rotate(90 198 47)"
                    fill="url(#paint0_radial_167_1206)"
                  />
                </g>
                <g id="Group 2393">
                  <g id="Rectangle 1154" filter="url(#filter1_di_167_1206)">
                    <path d="M237 60.8672C238.657 60.8672 240 62.2103 240 63.8672L240 81.4255C240 83.0823 238.657 84.4255 237 84.4255L209.08 84.4255L209.08 60.8672L237 60.8672Z" fill="url(#paint1_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155" d="M235.055 63.8125C236.159 63.8125 237.055 64.7079 237.055 65.8125L237.055 79.4812C237.055 80.5858 236.159 81.4812 235.055 81.4812L209.079 81.4812L209.079 63.8125L235.055 63.8125Z" fill="url(#paint2_linear_167_1206)" />
                </g>
                <g id="Group 2394">
                  <g id="Rectangle 1154_2" filter="url(#filter2_di_167_1206)">
                    <path d="M237 156.574C238.657 156.574 240 157.917 240 159.574L240 177.133C240 178.789 238.657 180.133 237 180.133L209.08 180.133L209.08 156.574L237 156.574Z" fill="url(#paint3_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_2" d="M235.055 159.52C236.159 159.52 237.055 160.415 237.055 161.52L237.055 175.188C237.055 176.293 236.159 177.188 235.055 177.188L209.079 177.188L209.079 159.52L235.055 159.52Z" fill="url(#paint4_linear_167_1206)" />
                </g>
                <g id="Group 2393_2">
                  <g id="Rectangle 1154_3" filter="url(#filter3_di_167_1206)">
                    <path d="M3 180.133C1.34315 180.133 1.76132e-07 178.79 3.93402e-07 177.133L2.69589e-06 159.575C2.91316e-06 157.918 1.34315 156.575 3 156.575L30.9202 156.575L30.9202 180.133L3 180.133Z" fill="url(#paint5_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_3" d="M4.94531 177.188C3.84074 177.188 2.94531 176.292 2.94531 175.187L2.94531 161.519C2.94531 160.414 3.84075 159.519 4.94531 159.519L30.9208 159.519L30.9208 177.188L4.94531 177.188Z" fill="url(#paint6_linear_167_1206)" />
                </g>
                <g id="Group 2394_2">
                  <g id="Rectangle 1154_4" filter="url(#filter4_di_167_1206)">
                    <path d="M3 84.4258C1.34315 84.4258 1.76132e-07 83.0826 3.93402e-07 81.4258L2.69589e-06 63.8675C2.91316e-06 62.2106 1.34315 60.8675 3 60.8675L30.9202 60.8675L30.9202 84.4258L3 84.4258Z" fill="url(#paint7_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_4" d="M4.94531 81.4805C3.84074 81.4805 2.94531 80.585 2.94531 79.4805L2.94531 65.8118C2.94531 64.7072 3.84075 63.8118 4.94531 63.8118L30.9208 63.8118L30.9208 81.4805L4.94531 81.4805Z" fill="url(#paint8_linear_167_1206)" />
                </g>
                <g id="Group 2393_3">
                  <g id="Rectangle 1154_5" filter="url(#filter5_di_167_1206)">
                    <path d="M60.3682 3.5C60.3682 1.84315 61.7113 0.5 63.3682 0.5L80.9264 0.500001C82.5833 0.500001 83.9264 1.84315 83.9264 3.5L83.9264 31.4202L60.3682 31.4202L60.3682 3.5Z" fill="url(#paint9_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_5" d="M63.3125 5.44531C63.3125 4.34074 64.2079 3.44531 65.3125 3.44531L78.9812 3.44531C80.0858 3.44531 80.9812 4.34074 80.9812 5.44531L80.9812 31.4208L63.3125 31.4208L63.3125 5.44531Z" fill="url(#paint10_linear_167_1206)" />
                </g>
                <g id="Group 2394_3">
                  <g id="Rectangle 1154_6" filter="url(#filter6_di_167_1206)">
                    <path d="M156.073 3.5C156.073 1.84315 157.416 0.5 159.073 0.5L176.632 0.500001C178.288 0.500001 179.632 1.84315 179.632 3.5L179.632 31.4202L156.073 31.4202L156.073 3.5Z" fill="url(#paint11_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_6" d="M159.019 5.44531C159.019 4.34074 159.914 3.44531 161.019 3.44531L174.687 3.44531C175.792 3.44531 176.687 4.34074 176.687 5.44531L176.687 31.4208L159.019 31.4208L159.019 5.44531Z" fill="url(#paint12_linear_167_1206)" />
                </g>
                <g id="Group 2393_4">
                  <g id="Rectangle 1154_7" filter="url(#filter7_di_167_1206)">
                    <path d="M179.632 237.5C179.632 239.157 178.289 240.5 176.632 240.5L159.074 240.5C157.417 240.5 156.074 239.157 156.074 237.5L156.074 209.58L179.632 209.58L179.632 237.5Z" fill="url(#paint13_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_7" d="M176.688 235.555C176.688 236.659 175.792 237.555 174.687 237.555L161.019 237.555C159.914 237.555 159.019 236.659 159.019 235.555L159.019 209.579L176.688 209.579L176.688 235.555Z" fill="url(#paint14_linear_167_1206)" />
                </g>
                <g id="Group 2394_4">
                  <g id="Rectangle 1154_8" filter="url(#filter8_di_167_1206)">
                    <path d="M83.9268 237.5C83.9268 239.157 82.5836 240.5 80.9268 240.5L63.3685 240.5C61.7116 240.5 60.3685 239.157 60.3685 237.5L60.3685 209.58L83.9268 209.58L83.9268 237.5Z" fill="url(#paint15_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_8" d="M80.9814 235.555C80.9814 236.659 80.086 237.555 78.9814 237.555L65.3127 237.555C64.2082 237.555 63.3127 236.659 63.3127 235.555L63.3127 209.579L80.9814 209.579L80.9814 235.555Z" fill="url(#paint16_linear_167_1206)" />
                </g>
                <g id="Group 2460">
                  <g id="Rectangle 1157">
                    <rect
                      x="197.72"
                      y="172.106"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 197.72 172.106)"
                      fill="#C4C4C4"
                    />
                    <rect
                      x="197.72"
                      y="172.106"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 197.72 172.106)"
                      fill="url(#paint17_linear_167_1206)"
                    />
                  </g>
                  <g id="Rectangle 1159" filter="url(#filter9_b_167_1206)">
                    <rect
                      x="198"
                      y="172"
                      width="8.00001"
                      height="155"
                      transform="rotate(90 198 172)"
                      fill="black"
                      fill-opacity="0.01"
                    />
                  </g>
                </g>
                <g id="Group 2461">
                  <g id="Mask Group" filter="url(#filter10_d_167_1206)">
                    <mask
                      id="mask0_167_1206"
                      style="mask-type:alpha"
                      maskUnits="userSpaceOnUse"
                      x="43"
                      y="157"
                      width="155"
                      height="8"
                    >
                      <rect
                        id="Rectangle 1158"
                        x="197.72"
                        y="157.185"
                        width="7.46114"
                        height="154.197"
                        transform="rotate(90 197.72 157.185)"
                        fill="url(#paint18_linear_167_1206)"
                      />
                    </mask>
                    <g mask="url(#mask0_167_1206)">
                      <g id="Rectangle 1159_2" filter="url(#filter11_f_167_1206)">
                        <rect
                          x="202.693"
                          y="157.185"
                          width="7.46114"
                          height="165.389"
                          transform="rotate(90 202.693 157.185)"
                          fill="url(#paint19_linear_167_1206)"
                        />
                      </g>
                    </g>
                  </g>
                  <g id="Rectangle 1158_2" filter="url(#filter12_b_167_1206)">
                    <rect
                      x="198"
                      y="157"
                      width="8.00001"
                      height="155"
                      transform="rotate(90 198 157)"
                      fill="black"
                      fill-opacity="0.01"
                    />
                  </g>
                </g>
                <g id="Group 2462">
                  <g id="Mask Group_2" filter="url(#filter13_d_167_1206)">
                    <mask
                      id="mask1_167_1206"
                      style="mask-type:alpha"
                      maskUnits="userSpaceOnUse"
                      x="43"
                      y="61"
                      width="155"
                      height="8"
                    >
                      <rect
                        id="Rectangle 1158_3"
                        x="197.72"
                        y="61.4326"
                        width="7.46114"
                        height="154.197"
                        transform="rotate(90 197.72 61.4326)"
                        fill="url(#paint20_linear_167_1206)"
                      />
                    </mask>
                    <g mask="url(#mask1_167_1206)">
                      <g id="Rectangle 1159_3" filter="url(#filter14_f_167_1206)">
                        <rect
                          x="202.693"
                          y="61.4326"
                          width="7.46114"
                          height="165.389"
                          transform="rotate(90 202.693 61.4326)"
                          fill="url(#paint21_linear_167_1206)"
                        />
                      </g>
                    </g>
                  </g>
                  <g id="Rectangle 1158_4" filter="url(#filter15_b_167_1206)">
                    <rect
                      x="197.72"
                      y="61.4326"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 197.72 61.4326)"
                      fill="black"
                      fill-opacity="0.01"
                    />
                  </g>
                </g>
                <g id="Group 2463">
                  <g id="Rectangle 1157_2">
                    <rect
                      x="197.72"
                      y="76.3545"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 197.72 76.3545)"
                      fill="#C4C4C4"
                    />
                    <rect
                      x="197.72"
                      y="76.3545"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 197.72 76.3545)"
                      fill="url(#paint22_linear_167_1206)"
                    />
                  </g>
                  <g id="Rectangle 1159_4" filter="url(#filter16_b_167_1206)">
                    <rect
                      x="197.72"
                      y="76.3545"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 197.72 76.3545)"
                      fill="black"
                      fill-opacity="0.01"
                    />
                  </g>
                </g>
                <g class="squareHover" id="light1">
                  <rect
                    id="Rectangle 1161"
                    x="43"
                    y="61"
                    width="155"
                    height="8"
                    fill="url(#paint23_linear_167_1206)"
                  />
                  <g id="Rectangle 1162" filter="url(#filter17_f_167_1206)">
                    <rect x="43" y="61" width="155" height="8" fill="url(#paint24_linear_167_1206)" />
                  </g>
                </g>
                <g class="squareHover" id="light2">
                  <rect
                    id="Rectangle 1161_2"
                    x="43"
                    y="76"
                    width="155"
                    height="8"
                    fill="url(#paint25_linear_167_1206)"
                  />
                  <g id="Rectangle 1162_2" filter="url(#filter18_f_167_1206)">
                    <rect x="43" y="76" width="155" height="8" fill="url(#paint26_linear_167_1206)" />
                  </g>
                </g>
                <g class="squareHover" id="light4">
                  <rect
                    id="Rectangle 1161_3"
                    x="43"
                    y="172"
                    width="155"
                    height="8"
                    fill="url(#paint27_linear_167_1206)"
                  />
                  <g id="Rectangle 1162_3" filter="url(#filter19_f_167_1206)">
                    <rect x="43" y="172" width="155" height="8" fill="url(#paint28_linear_167_1206)" />
                  </g>
                </g>
                <g class="squareHover" id="light3">
                  <rect
                    id="Rectangle 1161_4"
                    x="43"
                    y="157"
                    width="155"
                    height="8"
                    fill="url(#paint29_linear_167_1206)"
                  />
                  <g id="Rectangle 1162_4" filter="url(#filter20_f_167_1206)">
                    <rect x="43" y="157" width="155" height="8" fill="url(#paint30_linear_167_1206)" />
                  </g>
                </g>
              </g>
              <defs>
                <filter
                  id="filter0_di_167_1206"
                  x="-34"
                  y="-33"
                  width="308"
                  height="308"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="32.5" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.5 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="10" dy="10" />
                  <feGaussianBlur stdDeviation="7.5" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter1_di_167_1206"
                  x="205.08"
                  y="56.8672"
                  width="38.9199"
                  height="31.5586"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter2_di_167_1206"
                  x="205.08"
                  y="152.574"
                  width="38.9199"
                  height="31.5586"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter3_di_167_1206"
                  x="-4"
                  y="152.574"
                  width="38.9199"
                  height="31.5586"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter4_di_167_1206"
                  x="-4"
                  y="56.8672"
                  width="38.9199"
                  height="31.5586"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter5_di_167_1206"
                  x="56.3682"
                  y="-3.5"
                  width="31.5586"
                  height="38.9199"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter6_di_167_1206"
                  x="152.073"
                  y="-3.5"
                  width="31.5586"
                  height="38.9199"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter7_di_167_1206"
                  x="152.073"
                  y="205.58"
                  width="31.5586"
                  height="38.9199"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter8_di_167_1206"
                  x="56.3682"
                  y="205.58"
                  width="31.5586"
                  height="38.9199"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter9_b_167_1206"
                  x="40"
                  y="169"
                  width="161"
                  height="14"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feGaussianBlur in="BackgroundImage" stdDeviation="1.5" />
                  <feComposite in2="SourceAlpha" operator="in" result="effect1_backgroundBlur_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_backgroundBlur_167_1206" result="shape" />
                </filter>
                <filter
                  id="filter10_d_167_1206"
                  x="39.5225"
                  y="157.185"
                  width="162.197"
                  height="15.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dy="4" />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                </filter>
                <filter
                  id="filter11_f_167_1206"
                  x="34.3047"
                  y="154.185"
                  width="171.389"
                  height="13.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="1.5" result="effect1_foregroundBlur_167_1206" />
                </filter>
                <filter
                  id="filter12_b_167_1206"
                  x="40"
                  y="154"
                  width="161"
                  height="14"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feGaussianBlur in="BackgroundImage" stdDeviation="1.5" />
                  <feComposite in2="SourceAlpha" operator="in" result="effect1_backgroundBlur_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_backgroundBlur_167_1206" result="shape" />
                </filter>
                <filter
                  id="filter13_d_167_1206"
                  x="39.5225"
                  y="61.4326"
                  width="162.197"
                  height="15.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dy="4" />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                </filter>
                <filter
                  id="filter14_f_167_1206"
                  x="34.3047"
                  y="58.4326"
                  width="171.389"
                  height="13.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="1.5" result="effect1_foregroundBlur_167_1206" />
                </filter>
                <filter
                  id="filter15_b_167_1206"
                  x="40.5225"
                  y="58.4326"
                  width="160.197"
                  height="13.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feGaussianBlur in="BackgroundImage" stdDeviation="1.5" />
                  <feComposite in2="SourceAlpha" operator="in" result="effect1_backgroundBlur_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_backgroundBlur_167_1206" result="shape" />
                </filter>
                <filter
                  id="filter16_b_167_1206"
                  x="40.5225"
                  y="73.3545"
                  width="160.197"
                  height="13.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feGaussianBlur in="BackgroundImage" stdDeviation="1.5" />
                  <feComposite in2="SourceAlpha" operator="in" result="effect1_backgroundBlur_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_backgroundBlur_167_1206" result="shape" />
                </filter>
                <filter
                  id="filter17_f_167_1206"
                  x="28"
                  y="46"
                  width="185"
                  height="38"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="7.5" result="effect1_foregroundBlur_167_1206" />
                </filter>
                <filter
                  id="filter18_f_167_1206"
                  x="28"
                  y="61"
                  width="185"
                  height="38"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="7.5" result="effect1_foregroundBlur_167_1206" />
                </filter>
                <filter
                  id="filter19_f_167_1206"
                  x="28"
                  y="157"
                  width="185"
                  height="38"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="7.5" result="effect1_foregroundBlur_167_1206" />
                </filter>
                <filter
                  id="filter20_f_167_1206"
                  x="28"
                  y="142"
                  width="185"
                  height="38"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="7.5" result="effect1_foregroundBlur_167_1206" />
                </filter>
                <radialGradient
                  id="paint0_radial_167_1206"
                  cx="0"
                  cy="0"
                  r="1"
                  gradientUnits="userSpaceOnUse"
                  gradientTransform="translate(198 51.375) rotate(7.81946) scale(335.35 329.863)"
                >
                  <stop stop-color="#0B0B0D" />
                  <stop offset="1" stop-color="#303338" />
                </radialGradient>
                <linearGradient
                  id="paint1_linear_167_1206"
                  x1="240"
                  y1="72.6463"
                  x2="209.08"
                  y2="72.6463"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint2_linear_167_1206"
                  x1="237.055"
                  y1="72.6469"
                  x2="209.079"
                  y2="72.6469"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint3_linear_167_1206"
                  x1="240"
                  y1="168.353"
                  x2="209.08"
                  y2="168.353"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint4_linear_167_1206"
                  x1="237.055"
                  y1="168.354"
                  x2="209.079"
                  y2="168.354"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint5_linear_167_1206"
                  x1="1.54465e-06"
                  y1="168.354"
                  x2="30.9202"
                  y2="168.354"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint6_linear_167_1206"
                  x1="2.94531"
                  y1="168.353"
                  x2="30.9208"
                  y2="168.353"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint7_linear_167_1206"
                  x1="1.54465e-06"
                  y1="72.6466"
                  x2="30.9202"
                  y2="72.6466"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint8_linear_167_1206"
                  x1="2.94531"
                  y1="72.6461"
                  x2="30.9208"
                  y2="72.6461"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint9_linear_167_1206"
                  x1="72.1473"
                  y1="0.500001"
                  x2="72.1473"
                  y2="31.4202"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint10_linear_167_1206"
                  x1="72.1469"
                  y1="3.44531"
                  x2="72.1469"
                  y2="31.4208"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint11_linear_167_1206"
                  x1="167.852"
                  y1="0.500001"
                  x2="167.852"
                  y2="31.4202"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint12_linear_167_1206"
                  x1="167.853"
                  y1="3.44531"
                  x2="167.853"
                  y2="31.4208"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint13_linear_167_1206"
                  x1="167.853"
                  y1="240.5"
                  x2="167.853"
                  y2="209.58"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint14_linear_167_1206"
                  x1="167.853"
                  y1="237.555"
                  x2="167.853"
                  y2="209.579"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint15_linear_167_1206"
                  x1="72.1476"
                  y1="240.5"
                  x2="72.1476"
                  y2="209.58"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint16_linear_167_1206"
                  x1="72.1471"
                  y1="237.555"
                  x2="72.1471"
                  y2="209.579"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint17_linear_167_1206"
                  x1="205.181"
                  y1="223.713"
                  x2="197.72"
                  y2="223.713"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint18_linear_167_1206"
                  x1="205.181"
                  y1="208.791"
                  x2="197.72"
                  y2="208.791"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint19_linear_167_1206"
                  x1="210.154"
                  y1="212.536"
                  x2="202.693"
                  y2="212.536"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint20_linear_167_1206"
                  x1="205.181"
                  y1="113.039"
                  x2="197.72"
                  y2="113.039"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint21_linear_167_1206"
                  x1="210.154"
                  y1="116.784"
                  x2="202.693"
                  y2="116.784"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint22_linear_167_1206"
                  x1="205.181"
                  y1="127.961"
                  x2="197.72"
                  y2="127.961"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint23_linear_167_1206"
                  x1="61.6201"
                  y1="61"
                  x2="61.6201"
                  y2="69"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint24_linear_167_1206"
                  x1="61.6201"
                  y1="61"
                  x2="61.6201"
                  y2="69"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint25_linear_167_1206"
                  x1="61.6201"
                  y1="76"
                  x2="61.6201"
                  y2="84"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint26_linear_167_1206"
                  x1="61.6201"
                  y1="76"
                  x2="61.6201"
                  y2="84"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint27_linear_167_1206"
                  x1="61.6201"
                  y1="172"
                  x2="61.6201"
                  y2="180"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint28_linear_167_1206"
                  x1="61.6201"
                  y1="172"
                  x2="61.6201"
                  y2="180"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint29_linear_167_1206"
                  x1="61.6201"
                  y1="157"
                  x2="61.6201"
                  y2="165"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint30_linear_167_1206"
                  x1="61.6201"
                  y1="157"
                  x2="61.6201"
                  y2="165"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
              </defs>
            </svg> -->
            <svg viewBox="0 0 248 249">
              <g id="Group 2404">
                <g id="Group 2400">
                  <g id="Rectangle 1153" filter="url(#filter0_i_331_12138)">
                    <rect
                      x="213"
                      y="36"
                      width="178"
                      height="178"
                      transform="rotate(90 213 36)"
                      fill="#0D0F13"
                    />
                  </g>
                  <g id="Group 2399">
                    <g id="Group 2395">
                      <g id="Group 2393">
                        <g id="Rectangle 1154" filter="url(#filter1_di_331_12138)">
                          <path d="M241 64.8672C242.657 64.8672 244 66.2103 244 67.8672L244 85.4255C244 87.0823 242.657 88.4255 241 88.4255L213.08 88.4255L213.08 64.8672L241 64.8672Z" fill="url(#paint0_linear_331_12138)" />
                        </g>
                        <path id="Rectangle 1155" d="M239.055 67.8125C240.159 67.8125 241.055 68.7079 241.055 69.8125L241.055 83.4812C241.055 84.5858 240.159 85.4812 239.055 85.4812L213.079 85.4812L213.079 67.8125L239.055 67.8125Z" fill="url(#paint1_linear_331_12138)" />
                      </g>
                      <g id="Group 2394">
                        <g id="Rectangle 1154_2" filter="url(#filter2_di_331_12138)">
                          <path d="M241 160.574C242.657 160.574 244 161.917 244 163.574L244 181.133C244 182.789 242.657 184.133 241 184.133L213.08 184.133L213.08 160.574L241 160.574Z" fill="url(#paint2_linear_331_12138)" />
                        </g>
                        <path id="Rectangle 1155_2" d="M239.055 163.52C240.159 163.52 241.055 164.415 241.055 165.52L241.055 179.188C241.055 180.293 240.159 181.188 239.055 181.188L213.079 181.188L213.079 163.52L239.055 163.52Z" fill="url(#paint3_linear_331_12138)" />
                      </g>
                    </g>
                    <g id="Group 2398">
                      <g id="Group 2393_2">
                        <g id="Rectangle 1154_3" filter="url(#filter3_di_331_12138)">
                          <path d="M7 184.133C5.34315 184.133 4 182.79 4 181.133L4 163.575C4 161.918 5.34315 160.575 7 160.575L34.9202 160.575L34.9202 184.133L7 184.133Z" fill="url(#paint4_linear_331_12138)" />
                        </g>
                        <path id="Rectangle 1155_3" d="M8.94531 181.188C7.84074 181.188 6.94531 180.292 6.94531 179.187L6.94531 165.519C6.94531 164.414 7.84075 163.519 8.94531 163.519L34.9208 163.519L34.9208 181.188L8.94531 181.188Z" fill="url(#paint5_linear_331_12138)" />
                      </g>
                      <g id="Group 2394_2">
                        <g id="Rectangle 1154_4" filter="url(#filter4_di_331_12138)">
                          <path d="M7 88.4258C5.34315 88.4258 4 87.0826 4 85.4258L4 67.8675C4 66.2106 5.34315 64.8675 7 64.8675L34.9202 64.8675L34.9202 88.4258L7 88.4258Z" fill="url(#paint6_linear_331_12138)" />
                        </g>
                        <path id="Rectangle 1155_4" d="M8.94531 85.4805C7.84074 85.4805 6.94531 84.585 6.94531 83.4805L6.94531 69.8118C6.94531 68.7072 7.84075 67.8118 8.94531 67.8118L34.9208 67.8118L34.9208 85.4805L8.94531 85.4805Z" fill="url(#paint7_linear_331_12138)" />
                      </g>
                    </g>
                    <g id="Group 2396">
                      <g id="Group 2393_3">
                        <g id="Rectangle 1154_5" filter="url(#filter5_di_331_12138)">
                          <path d="M183.633 241.5C183.633 243.157 182.29 244.5 180.633 244.5L163.075 244.5C161.418 244.5 160.075 243.157 160.075 241.5L160.075 213.58L183.633 213.58L183.633 241.5Z" fill="url(#paint8_linear_331_12138)" />
                        </g>
                        <path id="Rectangle 1155_5" d="M180.688 239.555C180.688 240.659 179.792 241.555 178.687 241.555L165.019 241.555C163.914 241.555 163.019 240.659 163.019 239.555L163.019 213.579L180.688 213.579L180.688 239.555Z" fill="url(#paint9_linear_331_12138)" />
                      </g>
                      <g id="Group 2394_3">
                        <g id="Rectangle 1154_6" filter="url(#filter6_di_331_12138)">
                          <path d="M87.9297 241.5C87.9297 243.157 86.5865 244.5 84.9297 244.5L67.3714 244.5C65.7145 244.5 64.3714 243.157 64.3714 241.5L64.3714 213.58L87.9297 213.58L87.9297 241.5Z" fill="url(#paint10_linear_331_12138)" />
                        </g>
                        <path id="Rectangle 1155_6" d="M84.9844 239.555C84.9844 240.659 84.0889 241.555 82.9844 241.555L69.3157 241.555C68.2111 241.555 67.3157 240.659 67.3157 239.555L67.3157 213.579L84.9844 213.579L84.9844 239.555Z" fill="url(#paint11_linear_331_12138)" />
                      </g>
                    </g>
                    <g id="Group 2397">
                      <g id="Group 2393_4">
                        <g id="Rectangle 1154_7" filter="url(#filter7_di_331_12138)">
                          <path d="M64.3672 7.5C64.3672 5.84315 65.7103 4.5 67.3672 4.5L84.9255 4.5C86.5823 4.5 87.9255 5.84315 87.9255 7.5L87.9255 35.4202L64.3672 35.4202L64.3672 7.5Z" fill="url(#paint12_linear_331_12138)" />
                        </g>
                        <path id="Rectangle 1155_7" d="M67.3125 9.44531C67.3125 8.34074 68.2079 7.44531 69.3125 7.44531L82.9812 7.44531C84.0858 7.44531 84.9812 8.34074 84.9812 9.44531L84.9812 35.4208L67.3125 35.4208L67.3125 9.44531Z" fill="url(#paint13_linear_331_12138)" />
                      </g>
                      <g id="Group 2394_4">
                        <g id="Rectangle 1154_8" filter="url(#filter8_di_331_12138)">
                          <path d="M160.07 7.5C160.07 5.84315 161.413 4.5 163.07 4.5L180.629 4.5C182.285 4.5 183.629 5.84315 183.629 7.5L183.629 35.4202L160.07 35.4202L160.07 7.5Z" fill="url(#paint14_linear_331_12138)" />
                        </g>
                        <path id="Rectangle 1155_8" d="M163.016 9.44531C163.016 8.34074 163.911 7.44531 165.016 7.44531L178.684 7.44531C179.789 7.44531 180.684 8.34074 180.684 9.44531L180.684 35.4208L163.016 35.4208L163.016 9.44531Z" fill="url(#paint15_linear_331_12138)" />
                      </g>
                    </g>
                  </g>
                </g>
                <rect
                  id="Rectangle 1156"
                  x="202"
                  y="51"
                  width="150"
                  height="155"
                  transform="rotate(90 202 51)"
                  fill="url(#paint16_radial_331_12138)"
                />
                <g id="Group 2401">
                  <g id="Rectangle 1157">
                    <rect
                      x="201.719"
                      y="176.106"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 201.719 176.106)"
                      fill="#C4C4C4"
                    />
                    <rect
                      x="201.719"
                      y="176.106"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 201.719 176.106)"
                      fill="url(#paint17_linear_331_12138)"
                    />
                  </g>
                  <g id="Mask Group" filter="url(#filter9_d_331_12138)">
                    <mask
                      id="mask0_331_12138"
                      style="mask-type:alpha"
                      maskUnits="userSpaceOnUse"
                      x="47"
                      y="161"
                      width="155"
                      height="8"
                    >
                      <rect
                        id="Rectangle 1158"
                        x="201.719"
                        y="161.185"
                        width="7.46114"
                        height="154.197"
                        transform="rotate(90 201.719 161.185)"
                        fill="url(#paint18_linear_331_12138)"
                      />
                    </mask>
                    <g mask="url(#mask0_331_12138)">
                      <g id="Rectangle 1159" filter="url(#filter10_f_331_12138)">
                        <rect
                          x="206.691"
                          y="161.185"
                          width="7.46114"
                          height="165.389"
                          transform="rotate(90 206.691 161.185)"
                          fill="url(#paint19_linear_331_12138)"
                        />
                      </g>
                    </g>
                  </g>
                  <g id="Rectangle 1158_2" filter="url(#filter11_b_331_12138)">
                    <rect
                      x="202"
                      y="161"
                      width="8.00001"
                      height="155"
                      transform="rotate(90 202 161)"
                      fill="black"
                      fill-opacity="0.01"
                    />
                  </g>
                  <g id="Rectangle 1159_2" filter="url(#filter12_b_331_12138)">
                    <rect
                      x="202"
                      y="176"
                      width="8.00001"
                      height="155"
                      transform="rotate(90 202 176)"
                      fill="black"
                      fill-opacity="0.01"
                    />
                  </g>
                </g>
                <g id="Group 2402">
                  <g id="Rectangle 1157_2">
                    <rect
                      x="201.719"
                      y="80.3545"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 201.719 80.3545)"
                      fill="#C4C4C4"
                    />
                    <rect
                      x="201.719"
                      y="80.3545"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 201.719 80.3545)"
                      fill="url(#paint20_linear_331_12138)"
                    />
                  </g>
                  <g id="Mask Group_2" filter="url(#filter13_d_331_12138)">
                    <mask
                      id="mask1_331_12138"
                      style="mask-type:alpha"
                      maskUnits="userSpaceOnUse"
                      x="47"
                      y="65"
                      width="155"
                      height="8"
                    >
                      <rect
                        id="Rectangle 1158_3"
                        x="201.719"
                        y="65.4326"
                        width="7.46114"
                        height="154.197"
                        transform="rotate(90 201.719 65.4326)"
                        fill="url(#paint21_linear_331_12138)"
                      />
                    </mask>
                    <g mask="url(#mask1_331_12138)">
                      <g id="Rectangle 1159_3" filter="url(#filter14_f_331_12138)">
                        <rect
                          x="206.691"
                          y="65.4326"
                          width="7.46114"
                          height="165.389"
                          transform="rotate(90 206.691 65.4326)"
                          fill="url(#paint22_linear_331_12138)"
                        />
                      </g>
                    </g>
                  </g>
                  <g id="Rectangle 1158_4" filter="url(#filter15_b_331_12138)">
                    <rect
                      x="201.719"
                      y="65.4326"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 201.719 65.4326)"
                      fill="black"
                      fill-opacity="0.01"
                    />
                  </g>
                  <g id="Rectangle 1159_4" filter="url(#filter16_b_331_12138)">
                    <rect
                      x="201.719"
                      y="80.3545"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 201.719 80.3545)"
                      fill="black"
                      fill-opacity="0.01"
                    />
                  </g>
                </g>
                <g id="Group 2405" class="squareHover">
                  <rect
                    id="Rectangle 1161"
                    x="47"
                    y="65"
                    width="155"
                    height="8"
                    fill="url(#paint23_linear_331_12138)"
                  />
                  <g id="Rectangle 1162" filter="url(#filter17_f_331_12138)">
                    <rect x="47" y="65" width="155" height="8" fill="url(#paint24_linear_331_12138)" />
                  </g>
                </g>
                <g id="Group 2406" class="squareHover">
                  <rect
                    id="Rectangle 1161_2"
                    x="47"
                    y="80"
                    width="155"
                    height="8"
                    fill="url(#paint25_linear_331_12138)"
                  />
                  <g id="Rectangle 1162_2" filter="url(#filter18_f_331_12138)">
                    <rect x="47" y="80" width="155" height="8" fill="url(#paint26_linear_331_12138)" />
                  </g>
                </g>
                <g id="Group 2407" class="squareHover">
                  <rect
                    id="Rectangle 1161_3"
                    x="47"
                    y="176"
                    width="155"
                    height="8"
                    fill="url(#paint27_linear_331_12138)"
                  />
                  <g id="Rectangle 1162_3" filter="url(#filter19_f_331_12138)">
                    <rect x="47" y="176" width="155" height="8" fill="url(#paint28_linear_331_12138)" />
                  </g>
                </g>
                <g id="Group 2408" class="squareHover">
                  <rect
                    id="Rectangle 1161_4"
                    x="47"
                    y="161"
                    width="155"
                    height="8"
                    fill="url(#paint29_linear_331_12138)"
                  />
                  <g id="Rectangle 1162_4" filter="url(#filter20_f_331_12138)">
                    <rect x="47" y="161" width="155" height="8" fill="url(#paint30_linear_331_12138)" />
                  </g>
                </g>
              </g>
              <defs>
                <filter
                  id="filter0_i_331_12138"
                  x="35"
                  y="36"
                  width="188"
                  height="188"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="10" dy="10" />
                  <feGaussianBlur stdDeviation="7.5" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect1_innerShadow_331_12138" />
                </filter>
                <filter
                  id="filter1_di_331_12138"
                  x="209.078"
                  y="60.8672"
                  width="38.9219"
                  height="31.5586"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_331_12138" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_331_12138" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_331_12138" />
                </filter>
                <filter
                  id="filter2_di_331_12138"
                  x="209.078"
                  y="156.574"
                  width="38.9219"
                  height="31.5586"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_331_12138" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_331_12138" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_331_12138" />
                </filter>
                <filter
                  id="filter3_di_331_12138"
                  x="0"
                  y="156.574"
                  width="38.9219"
                  height="31.5586"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_331_12138" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_331_12138" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_331_12138" />
                </filter>
                <filter
                  id="filter4_di_331_12138"
                  x="0"
                  y="60.8672"
                  width="38.9219"
                  height="31.5586"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_331_12138" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_331_12138" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_331_12138" />
                </filter>
                <filter
                  id="filter5_di_331_12138"
                  x="156.074"
                  y="209.58"
                  width="31.5586"
                  height="38.9199"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_331_12138" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_331_12138" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_331_12138" />
                </filter>
                <filter
                  id="filter6_di_331_12138"
                  x="60.3711"
                  y="209.58"
                  width="31.5586"
                  height="38.9199"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_331_12138" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_331_12138" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_331_12138" />
                </filter>
                <filter
                  id="filter7_di_331_12138"
                  x="60.3672"
                  y="0.5"
                  width="31.5586"
                  height="38.9199"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_331_12138" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_331_12138" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_331_12138" />
                </filter>
                <filter
                  id="filter8_di_331_12138"
                  x="156.07"
                  y="0.5"
                  width="31.5586"
                  height="38.9199"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_331_12138" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_331_12138" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_331_12138" />
                </filter>
                <filter
                  id="filter9_d_331_12138"
                  x="43.5234"
                  y="161.185"
                  width="162.195"
                  height="15.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dy="4" />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_331_12138" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_331_12138" result="shape" />
                </filter>
                <filter
                  id="filter10_f_331_12138"
                  x="38.3047"
                  y="158.185"
                  width="171.387"
                  height="13.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="1.5" result="effect1_foregroundBlur_331_12138" />
                </filter>
                <filter
                  id="filter11_b_331_12138"
                  x="44"
                  y="158"
                  width="161"
                  height="14"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feGaussianBlur in="BackgroundImage" stdDeviation="1.5" />
                  <feComposite in2="SourceAlpha" operator="in" result="effect1_backgroundBlur_331_12138" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_backgroundBlur_331_12138" result="shape" />
                </filter>
                <filter
                  id="filter12_b_331_12138"
                  x="44"
                  y="173"
                  width="161"
                  height="14"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feGaussianBlur in="BackgroundImage" stdDeviation="1.5" />
                  <feComposite in2="SourceAlpha" operator="in" result="effect1_backgroundBlur_331_12138" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_backgroundBlur_331_12138" result="shape" />
                </filter>
                <filter
                  id="filter13_d_331_12138"
                  x="43.5234"
                  y="65.4326"
                  width="162.195"
                  height="15.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dy="4" />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_331_12138" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_331_12138" result="shape" />
                </filter>
                <filter
                  id="filter14_f_331_12138"
                  x="38.3047"
                  y="62.4326"
                  width="171.387"
                  height="13.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="1.5" result="effect1_foregroundBlur_331_12138" />
                </filter>
                <filter
                  id="filter15_b_331_12138"
                  x="44.5234"
                  y="62.4326"
                  width="160.195"
                  height="13.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feGaussianBlur in="BackgroundImage" stdDeviation="1.5" />
                  <feComposite in2="SourceAlpha" operator="in" result="effect1_backgroundBlur_331_12138" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_backgroundBlur_331_12138" result="shape" />
                </filter>
                <filter
                  id="filter16_b_331_12138"
                  x="44.5234"
                  y="77.3545"
                  width="160.195"
                  height="13.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feGaussianBlur in="BackgroundImage" stdDeviation="1.5" />
                  <feComposite in2="SourceAlpha" operator="in" result="effect1_backgroundBlur_331_12138" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_backgroundBlur_331_12138" result="shape" />
                </filter>
                <filter
                  id="filter17_f_331_12138"
                  x="32"
                  y="50"
                  width="185"
                  height="38"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="7.5" result="effect1_foregroundBlur_331_12138" />
                </filter>
                <filter
                  id="filter18_f_331_12138"
                  x="32"
                  y="65"
                  width="185"
                  height="38"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="7.5" result="effect1_foregroundBlur_331_12138" />
                </filter>
                <filter
                  id="filter19_f_331_12138"
                  x="32"
                  y="161"
                  width="185"
                  height="38"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="7.5" result="effect1_foregroundBlur_331_12138" />
                </filter>
                <filter
                  id="filter20_f_331_12138"
                  x="32"
                  y="146"
                  width="185"
                  height="38"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="7.5" result="effect1_foregroundBlur_331_12138" />
                </filter>
                <linearGradient
                  id="paint0_linear_331_12138"
                  x1="244"
                  y1="76.6463"
                  x2="213.08"
                  y2="76.6463"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint1_linear_331_12138"
                  x1="241.055"
                  y1="76.6469"
                  x2="213.079"
                  y2="76.6469"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint2_linear_331_12138"
                  x1="244"
                  y1="172.353"
                  x2="213.08"
                  y2="172.353"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint3_linear_331_12138"
                  x1="241.055"
                  y1="172.354"
                  x2="213.079"
                  y2="172.354"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint4_linear_331_12138"
                  x1="4"
                  y1="172.354"
                  x2="34.9202"
                  y2="172.354"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint5_linear_331_12138"
                  x1="6.94531"
                  y1="172.353"
                  x2="34.9208"
                  y2="172.353"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint6_linear_331_12138"
                  x1="4"
                  y1="76.6466"
                  x2="34.9202"
                  y2="76.6466"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint7_linear_331_12138"
                  x1="6.94531"
                  y1="76.6461"
                  x2="34.9208"
                  y2="76.6461"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint8_linear_331_12138"
                  x1="171.854"
                  y1="244.5"
                  x2="171.854"
                  y2="213.58"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint9_linear_331_12138"
                  x1="171.853"
                  y1="241.555"
                  x2="171.853"
                  y2="213.579"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint10_linear_331_12138"
                  x1="76.1505"
                  y1="244.5"
                  x2="76.1505"
                  y2="213.58"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint11_linear_331_12138"
                  x1="76.15"
                  y1="241.555"
                  x2="76.15"
                  y2="213.579"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint12_linear_331_12138"
                  x1="76.1463"
                  y1="4.5"
                  x2="76.1463"
                  y2="35.4202"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint13_linear_331_12138"
                  x1="76.1469"
                  y1="7.44531"
                  x2="76.1469"
                  y2="35.4208"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint14_linear_331_12138"
                  x1="171.849"
                  y1="4.5"
                  x2="171.849"
                  y2="35.4202"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint15_linear_331_12138"
                  x1="171.85"
                  y1="7.44531"
                  x2="171.85"
                  y2="35.4208"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <radialGradient
                  id="paint16_radial_331_12138"
                  cx="0"
                  cy="0"
                  r="1"
                  gradientUnits="userSpaceOnUse"
                  gradientTransform="translate(202 55.375) rotate(7.81946) scale(335.35 329.863)"
                >
                  <stop stop-color="#0B0B0D" />
                  <stop offset="1" stop-color="#303338" />
                </radialGradient>
                <linearGradient
                  id="paint17_linear_331_12138"
                  x1="209.18"
                  y1="227.713"
                  x2="201.719"
                  y2="227.713"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint18_linear_331_12138"
                  x1="209.18"
                  y1="212.791"
                  x2="201.719"
                  y2="212.791"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint19_linear_331_12138"
                  x1="214.153"
                  y1="216.536"
                  x2="206.691"
                  y2="216.536"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint20_linear_331_12138"
                  x1="209.18"
                  y1="131.961"
                  x2="201.719"
                  y2="131.961"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint21_linear_331_12138"
                  x1="209.18"
                  y1="117.039"
                  x2="201.719"
                  y2="117.039"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint22_linear_331_12138"
                  x1="214.153"
                  y1="120.784"
                  x2="206.691"
                  y2="120.784"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint23_linear_331_12138"
                  x1="65.6201"
                  y1="65"
                  x2="65.6201"
                  y2="73"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint24_linear_331_12138"
                  x1="65.6201"
                  y1="65"
                  x2="65.6201"
                  y2="73"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint25_linear_331_12138"
                  x1="65.6201"
                  y1="80"
                  x2="65.6201"
                  y2="88"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint26_linear_331_12138"
                  x1="65.6201"
                  y1="80"
                  x2="65.6201"
                  y2="88"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint27_linear_331_12138"
                  x1="65.6201"
                  y1="176"
                  x2="65.6201"
                  y2="184"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint28_linear_331_12138"
                  x1="65.6201"
                  y1="176"
                  x2="65.6201"
                  y2="184"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint29_linear_331_12138"
                  x1="65.6201"
                  y1="161"
                  x2="65.6201"
                  y2="169"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint30_linear_331_12138"
                  x1="65.6201"
                  y1="161"
                  x2="65.6201"
                  y2="169"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
              </defs>
            </svg>
            <p>
              {{ item.text }}
            </p>
          </div>
          <!-- <div class="mainPage_block5_anim_square s1">
            <svg viewBox="0 0 240 241">
              <g id="Group 2412">
                <g id="Group 2465">
                  <g id="Rectangle 1153" filter="url(#filter0_di_167_1206)">
                    <rect
                      x="209"
                      y="32"
                      width="178"
                      height="178"
                      transform="rotate(90 209 32)"
                      fill="#0D0F13"
                    />
                  </g>
                  <rect
                    id="Rectangle 1156"
                    x="198"
                    y="47"
                    width="150"
                    height="155"
                    transform="rotate(90 198 47)"
                    fill="url(#paint0_radial_167_1206)"
                  />
                </g>
                <g id="Group 2393">
                  <g id="Rectangle 1154" filter="url(#filter1_di_167_1206)">
                    <path d="M237 60.8672C238.657 60.8672 240 62.2103 240 63.8672L240 81.4255C240 83.0823 238.657 84.4255 237 84.4255L209.08 84.4255L209.08 60.8672L237 60.8672Z" fill="url(#paint1_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155" d="M235.055 63.8125C236.159 63.8125 237.055 64.7079 237.055 65.8125L237.055 79.4812C237.055 80.5858 236.159 81.4812 235.055 81.4812L209.079 81.4812L209.079 63.8125L235.055 63.8125Z" fill="url(#paint2_linear_167_1206)" />
                </g>
                <g id="Group 2394">
                  <g id="Rectangle 1154_2" filter="url(#filter2_di_167_1206)">
                    <path d="M237 156.574C238.657 156.574 240 157.917 240 159.574L240 177.133C240 178.789 238.657 180.133 237 180.133L209.08 180.133L209.08 156.574L237 156.574Z" fill="url(#paint3_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_2" d="M235.055 159.52C236.159 159.52 237.055 160.415 237.055 161.52L237.055 175.188C237.055 176.293 236.159 177.188 235.055 177.188L209.079 177.188L209.079 159.52L235.055 159.52Z" fill="url(#paint4_linear_167_1206)" />
                </g>
                <g id="Group 2393_2">
                  <g id="Rectangle 1154_3" filter="url(#filter3_di_167_1206)">
                    <path d="M3 180.133C1.34315 180.133 1.76132e-07 178.79 3.93402e-07 177.133L2.69589e-06 159.575C2.91316e-06 157.918 1.34315 156.575 3 156.575L30.9202 156.575L30.9202 180.133L3 180.133Z" fill="url(#paint5_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_3" d="M4.94531 177.188C3.84074 177.188 2.94531 176.292 2.94531 175.187L2.94531 161.519C2.94531 160.414 3.84075 159.519 4.94531 159.519L30.9208 159.519L30.9208 177.188L4.94531 177.188Z" fill="url(#paint6_linear_167_1206)" />
                </g>
                <g id="Group 2394_2">
                  <g id="Rectangle 1154_4" filter="url(#filter4_di_167_1206)">
                    <path d="M3 84.4258C1.34315 84.4258 1.76132e-07 83.0826 3.93402e-07 81.4258L2.69589e-06 63.8675C2.91316e-06 62.2106 1.34315 60.8675 3 60.8675L30.9202 60.8675L30.9202 84.4258L3 84.4258Z" fill="url(#paint7_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_4" d="M4.94531 81.4805C3.84074 81.4805 2.94531 80.585 2.94531 79.4805L2.94531 65.8118C2.94531 64.7072 3.84075 63.8118 4.94531 63.8118L30.9208 63.8118L30.9208 81.4805L4.94531 81.4805Z" fill="url(#paint8_linear_167_1206)" />
                </g>
                <g id="Group 2393_3">
                  <g id="Rectangle 1154_5" filter="url(#filter5_di_167_1206)">
                    <path d="M60.3682 3.5C60.3682 1.84315 61.7113 0.5 63.3682 0.5L80.9264 0.500001C82.5833 0.500001 83.9264 1.84315 83.9264 3.5L83.9264 31.4202L60.3682 31.4202L60.3682 3.5Z" fill="url(#paint9_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_5" d="M63.3125 5.44531C63.3125 4.34074 64.2079 3.44531 65.3125 3.44531L78.9812 3.44531C80.0858 3.44531 80.9812 4.34074 80.9812 5.44531L80.9812 31.4208L63.3125 31.4208L63.3125 5.44531Z" fill="url(#paint10_linear_167_1206)" />
                </g>
                <g id="Group 2394_3">
                  <g id="Rectangle 1154_6" filter="url(#filter6_di_167_1206)">
                    <path d="M156.073 3.5C156.073 1.84315 157.416 0.5 159.073 0.5L176.632 0.500001C178.288 0.500001 179.632 1.84315 179.632 3.5L179.632 31.4202L156.073 31.4202L156.073 3.5Z" fill="url(#paint11_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_6" d="M159.019 5.44531C159.019 4.34074 159.914 3.44531 161.019 3.44531L174.687 3.44531C175.792 3.44531 176.687 4.34074 176.687 5.44531L176.687 31.4208L159.019 31.4208L159.019 5.44531Z" fill="url(#paint12_linear_167_1206)" />
                </g>
                <g id="Group 2393_4">
                  <g id="Rectangle 1154_7" filter="url(#filter7_di_167_1206)">
                    <path d="M179.632 237.5C179.632 239.157 178.289 240.5 176.632 240.5L159.074 240.5C157.417 240.5 156.074 239.157 156.074 237.5L156.074 209.58L179.632 209.58L179.632 237.5Z" fill="url(#paint13_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_7" d="M176.688 235.555C176.688 236.659 175.792 237.555 174.687 237.555L161.019 237.555C159.914 237.555 159.019 236.659 159.019 235.555L159.019 209.579L176.688 209.579L176.688 235.555Z" fill="url(#paint14_linear_167_1206)" />
                </g>
                <g id="Group 2394_4">
                  <g id="Rectangle 1154_8" filter="url(#filter8_di_167_1206)">
                    <path d="M83.9268 237.5C83.9268 239.157 82.5836 240.5 80.9268 240.5L63.3685 240.5C61.7116 240.5 60.3685 239.157 60.3685 237.5L60.3685 209.58L83.9268 209.58L83.9268 237.5Z" fill="url(#paint15_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_8" d="M80.9814 235.555C80.9814 236.659 80.086 237.555 78.9814 237.555L65.3127 237.555C64.2082 237.555 63.3127 236.659 63.3127 235.555L63.3127 209.579L80.9814 209.579L80.9814 235.555Z" fill="url(#paint16_linear_167_1206)" />
                </g>
                <g id="Group 2460">
                  <g id="Rectangle 1157">
                    <rect
                      x="197.72"
                      y="172.106"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 197.72 172.106)"
                      fill="#C4C4C4"
                    />
                    <rect
                      x="197.72"
                      y="172.106"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 197.72 172.106)"
                      fill="url(#paint17_linear_167_1206)"
                    />
                  </g>
                  <g id="Rectangle 1159" filter="url(#filter9_b_167_1206)">
                    <rect
                      x="198"
                      y="172"
                      width="8.00001"
                      height="155"
                      transform="rotate(90 198 172)"
                      fill="black"
                      fill-opacity="0.01"
                    />
                  </g>
                </g>
                <g id="Group 2461">
                  <g id="Mask Group" filter="url(#filter10_d_167_1206)">
                    <mask
                      id="mask0_167_1206"
                      style="mask-type:alpha"
                      maskUnits="userSpaceOnUse"
                      x="43"
                      y="157"
                      width="155"
                      height="8"
                    >
                      <rect
                        id="Rectangle 1158"
                        x="197.72"
                        y="157.185"
                        width="7.46114"
                        height="154.197"
                        transform="rotate(90 197.72 157.185)"
                        fill="url(#paint18_linear_167_1206)"
                      />
                    </mask>
                    <g mask="url(#mask0_167_1206)">
                      <g id="Rectangle 1159_2" filter="url(#filter11_f_167_1206)">
                        <rect
                          x="202.693"
                          y="157.185"
                          width="7.46114"
                          height="165.389"
                          transform="rotate(90 202.693 157.185)"
                          fill="url(#paint19_linear_167_1206)"
                        />
                      </g>
                    </g>
                  </g>
                  <g id="Rectangle 1158_2" filter="url(#filter12_b_167_1206)">
                    <rect
                      x="198"
                      y="157"
                      width="8.00001"
                      height="155"
                      transform="rotate(90 198 157)"
                      fill="black"
                      fill-opacity="0.01"
                    />
                  </g>
                </g>
                <g id="Group 2462">
                  <g id="Mask Group_2" filter="url(#filter13_d_167_1206)">
                    <mask
                      id="mask1_167_1206"
                      style="mask-type:alpha"
                      maskUnits="userSpaceOnUse"
                      x="43"
                      y="61"
                      width="155"
                      height="8"
                    >
                      <rect
                        id="Rectangle 1158_3"
                        x="197.72"
                        y="61.4326"
                        width="7.46114"
                        height="154.197"
                        transform="rotate(90 197.72 61.4326)"
                        fill="url(#paint20_linear_167_1206)"
                      />
                    </mask>
                    <g mask="url(#mask1_167_1206)">
                      <g id="Rectangle 1159_3" filter="url(#filter14_f_167_1206)">
                        <rect
                          x="202.693"
                          y="61.4326"
                          width="7.46114"
                          height="165.389"
                          transform="rotate(90 202.693 61.4326)"
                          fill="url(#paint21_linear_167_1206)"
                        />
                      </g>
                    </g>
                  </g>
                  <g id="Rectangle 1158_4" filter="url(#filter15_b_167_1206)">
                    <rect
                      x="197.72"
                      y="61.4326"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 197.72 61.4326)"
                      fill="black"
                      fill-opacity="0.01"
                    />
                  </g>
                </g>
                <g id="Group 2463">
                  <g id="Rectangle 1157_2">
                    <rect
                      x="197.72"
                      y="76.3545"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 197.72 76.3545)"
                      fill="#C4C4C4"
                    />
                    <rect
                      x="197.72"
                      y="76.3545"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 197.72 76.3545)"
                      fill="url(#paint22_linear_167_1206)"
                    />
                  </g>
                  <g id="Rectangle 1159_4" filter="url(#filter16_b_167_1206)">
                    <rect
                      x="197.72"
                      y="76.3545"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 197.72 76.3545)"
                      fill="black"
                      fill-opacity="0.01"
                    />
                  </g>
                </g>
                <g class="squareHover" id="light1">
                  <rect
                    id="Rectangle 1161"
                    x="43"
                    y="61"
                    width="155"
                    height="8"
                    fill="url(#paint23_linear_167_1206)"
                  />
                  <g id="Rectangle 1162" filter="url(#filter17_f_167_1206)">
                    <rect x="43" y="61" width="155" height="8" fill="url(#paint24_linear_167_1206)" />
                  </g>
                </g>
                <g class="squareHover" id="light2">
                  <rect
                    id="Rectangle 1161_2"
                    x="43"
                    y="76"
                    width="155"
                    height="8"
                    fill="url(#paint25_linear_167_1206)"
                  />
                  <g id="Rectangle 1162_2" filter="url(#filter18_f_167_1206)">
                    <rect x="43" y="76" width="155" height="8" fill="url(#paint26_linear_167_1206)" />
                  </g>
                </g>
                <g class="squareHover" id="light4">
                  <rect
                    id="Rectangle 1161_3"
                    x="43"
                    y="172"
                    width="155"
                    height="8"
                    fill="url(#paint27_linear_167_1206)"
                  />
                  <g id="Rectangle 1162_3" filter="url(#filter19_f_167_1206)">
                    <rect x="43" y="172" width="155" height="8" fill="url(#paint28_linear_167_1206)" />
                  </g>
                </g>
                <g class="squareHover" id="light3">
                  <rect
                    id="Rectangle 1161_4"
                    x="43"
                    y="157"
                    width="155"
                    height="8"
                    fill="url(#paint29_linear_167_1206)"
                  />
                  <g id="Rectangle 1162_4" filter="url(#filter20_f_167_1206)">
                    <rect x="43" y="157" width="155" height="8" fill="url(#paint30_linear_167_1206)" />
                  </g>
                </g>
              </g>
              <defs>
                <filter
                  id="filter0_di_167_1206"
                  x="-34"
                  y="-33"
                  width="308"
                  height="308"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="32.5" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.5 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="10" dy="10" />
                  <feGaussianBlur stdDeviation="7.5" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter1_di_167_1206"
                  x="205.08"
                  y="56.8672"
                  width="38.9199"
                  height="31.5586"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter2_di_167_1206"
                  x="205.08"
                  y="152.574"
                  width="38.9199"
                  height="31.5586"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter3_di_167_1206"
                  x="-4"
                  y="152.574"
                  width="38.9199"
                  height="31.5586"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter4_di_167_1206"
                  x="-4"
                  y="56.8672"
                  width="38.9199"
                  height="31.5586"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter5_di_167_1206"
                  x="56.3682"
                  y="-3.5"
                  width="31.5586"
                  height="38.9199"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter6_di_167_1206"
                  x="152.073"
                  y="-3.5"
                  width="31.5586"
                  height="38.9199"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter7_di_167_1206"
                  x="152.073"
                  y="205.58"
                  width="31.5586"
                  height="38.9199"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter8_di_167_1206"
                  x="56.3682"
                  y="205.58"
                  width="31.5586"
                  height="38.9199"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter9_b_167_1206"
                  x="40"
                  y="169"
                  width="161"
                  height="14"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feGaussianBlur in="BackgroundImage" stdDeviation="1.5" />
                  <feComposite in2="SourceAlpha" operator="in" result="effect1_backgroundBlur_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_backgroundBlur_167_1206" result="shape" />
                </filter>
                <filter
                  id="filter10_d_167_1206"
                  x="39.5225"
                  y="157.185"
                  width="162.197"
                  height="15.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dy="4" />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                </filter>
                <filter
                  id="filter11_f_167_1206"
                  x="34.3047"
                  y="154.185"
                  width="171.389"
                  height="13.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="1.5" result="effect1_foregroundBlur_167_1206" />
                </filter>
                <filter
                  id="filter12_b_167_1206"
                  x="40"
                  y="154"
                  width="161"
                  height="14"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feGaussianBlur in="BackgroundImage" stdDeviation="1.5" />
                  <feComposite in2="SourceAlpha" operator="in" result="effect1_backgroundBlur_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_backgroundBlur_167_1206" result="shape" />
                </filter>
                <filter
                  id="filter13_d_167_1206"
                  x="39.5225"
                  y="61.4326"
                  width="162.197"
                  height="15.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dy="4" />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                </filter>
                <filter
                  id="filter14_f_167_1206"
                  x="34.3047"
                  y="58.4326"
                  width="171.389"
                  height="13.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="1.5" result="effect1_foregroundBlur_167_1206" />
                </filter>
                <filter
                  id="filter15_b_167_1206"
                  x="40.5225"
                  y="58.4326"
                  width="160.197"
                  height="13.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feGaussianBlur in="BackgroundImage" stdDeviation="1.5" />
                  <feComposite in2="SourceAlpha" operator="in" result="effect1_backgroundBlur_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_backgroundBlur_167_1206" result="shape" />
                </filter>
                <filter
                  id="filter16_b_167_1206"
                  x="40.5225"
                  y="73.3545"
                  width="160.197"
                  height="13.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feGaussianBlur in="BackgroundImage" stdDeviation="1.5" />
                  <feComposite in2="SourceAlpha" operator="in" result="effect1_backgroundBlur_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_backgroundBlur_167_1206" result="shape" />
                </filter>
                <filter
                  id="filter17_f_167_1206"
                  x="28"
                  y="46"
                  width="185"
                  height="38"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="7.5" result="effect1_foregroundBlur_167_1206" />
                </filter>
                <filter
                  id="filter18_f_167_1206"
                  x="28"
                  y="61"
                  width="185"
                  height="38"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="7.5" result="effect1_foregroundBlur_167_1206" />
                </filter>
                <filter
                  id="filter19_f_167_1206"
                  x="28"
                  y="157"
                  width="185"
                  height="38"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="7.5" result="effect1_foregroundBlur_167_1206" />
                </filter>
                <filter
                  id="filter20_f_167_1206"
                  x="28"
                  y="142"
                  width="185"
                  height="38"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="7.5" result="effect1_foregroundBlur_167_1206" />
                </filter>
                <radialGradient
                  id="paint0_radial_167_1206"
                  cx="0"
                  cy="0"
                  r="1"
                  gradientUnits="userSpaceOnUse"
                  gradientTransform="translate(198 51.375) rotate(7.81946) scale(335.35 329.863)"
                >
                  <stop stop-color="#0B0B0D" />
                  <stop offset="1" stop-color="#303338" />
                </radialGradient>
                <linearGradient
                  id="paint1_linear_167_1206"
                  x1="240"
                  y1="72.6463"
                  x2="209.08"
                  y2="72.6463"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint2_linear_167_1206"
                  x1="237.055"
                  y1="72.6469"
                  x2="209.079"
                  y2="72.6469"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint3_linear_167_1206"
                  x1="240"
                  y1="168.353"
                  x2="209.08"
                  y2="168.353"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint4_linear_167_1206"
                  x1="237.055"
                  y1="168.354"
                  x2="209.079"
                  y2="168.354"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint5_linear_167_1206"
                  x1="1.54465e-06"
                  y1="168.354"
                  x2="30.9202"
                  y2="168.354"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint6_linear_167_1206"
                  x1="2.94531"
                  y1="168.353"
                  x2="30.9208"
                  y2="168.353"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint7_linear_167_1206"
                  x1="1.54465e-06"
                  y1="72.6466"
                  x2="30.9202"
                  y2="72.6466"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint8_linear_167_1206"
                  x1="2.94531"
                  y1="72.6461"
                  x2="30.9208"
                  y2="72.6461"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint9_linear_167_1206"
                  x1="72.1473"
                  y1="0.500001"
                  x2="72.1473"
                  y2="31.4202"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint10_linear_167_1206"
                  x1="72.1469"
                  y1="3.44531"
                  x2="72.1469"
                  y2="31.4208"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint11_linear_167_1206"
                  x1="167.852"
                  y1="0.500001"
                  x2="167.852"
                  y2="31.4202"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint12_linear_167_1206"
                  x1="167.853"
                  y1="3.44531"
                  x2="167.853"
                  y2="31.4208"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint13_linear_167_1206"
                  x1="167.853"
                  y1="240.5"
                  x2="167.853"
                  y2="209.58"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint14_linear_167_1206"
                  x1="167.853"
                  y1="237.555"
                  x2="167.853"
                  y2="209.579"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint15_linear_167_1206"
                  x1="72.1476"
                  y1="240.5"
                  x2="72.1476"
                  y2="209.58"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint16_linear_167_1206"
                  x1="72.1471"
                  y1="237.555"
                  x2="72.1471"
                  y2="209.579"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint17_linear_167_1206"
                  x1="205.181"
                  y1="223.713"
                  x2="197.72"
                  y2="223.713"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint18_linear_167_1206"
                  x1="205.181"
                  y1="208.791"
                  x2="197.72"
                  y2="208.791"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint19_linear_167_1206"
                  x1="210.154"
                  y1="212.536"
                  x2="202.693"
                  y2="212.536"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint20_linear_167_1206"
                  x1="205.181"
                  y1="113.039"
                  x2="197.72"
                  y2="113.039"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint21_linear_167_1206"
                  x1="210.154"
                  y1="116.784"
                  x2="202.693"
                  y2="116.784"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint22_linear_167_1206"
                  x1="205.181"
                  y1="127.961"
                  x2="197.72"
                  y2="127.961"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint23_linear_167_1206"
                  x1="61.6201"
                  y1="61"
                  x2="61.6201"
                  y2="69"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint24_linear_167_1206"
                  x1="61.6201"
                  y1="61"
                  x2="61.6201"
                  y2="69"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint25_linear_167_1206"
                  x1="61.6201"
                  y1="76"
                  x2="61.6201"
                  y2="84"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint26_linear_167_1206"
                  x1="61.6201"
                  y1="76"
                  x2="61.6201"
                  y2="84"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint27_linear_167_1206"
                  x1="61.6201"
                  y1="172"
                  x2="61.6201"
                  y2="180"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint28_linear_167_1206"
                  x1="61.6201"
                  y1="172"
                  x2="61.6201"
                  y2="180"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint29_linear_167_1206"
                  x1="61.6201"
                  y1="157"
                  x2="61.6201"
                  y2="165"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint30_linear_167_1206"
                  x1="61.6201"
                  y1="157"
                  x2="61.6201"
                  y2="165"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
              </defs>
            </svg>
            <p>
              {{ datablock5.square_text[0] }}
            </p>
          </div>
          <div class="mainPage_block5_anim_square s2">
            <svg viewBox="0 0 240 241">
              <g id="Group 2412">
                <g id="Group 2465">
                  <g id="Rectangle 1153" filter="url(#filter0_di_167_1206)">
                    <rect
                      x="209"
                      y="32"
                      width="178"
                      height="178"
                      transform="rotate(90 209 32)"
                      fill="#0D0F13"
                    />
                  </g>
                  <rect
                    id="Rectangle 1156"
                    x="198"
                    y="47"
                    width="150"
                    height="155"
                    transform="rotate(90 198 47)"
                    fill="url(#paint0_radial_167_1206)"
                  />
                </g>
                <g id="Group 2393">
                  <g id="Rectangle 1154" filter="url(#filter1_di_167_1206)">
                    <path d="M237 60.8672C238.657 60.8672 240 62.2103 240 63.8672L240 81.4255C240 83.0823 238.657 84.4255 237 84.4255L209.08 84.4255L209.08 60.8672L237 60.8672Z" fill="url(#paint1_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155" d="M235.055 63.8125C236.159 63.8125 237.055 64.7079 237.055 65.8125L237.055 79.4812C237.055 80.5858 236.159 81.4812 235.055 81.4812L209.079 81.4812L209.079 63.8125L235.055 63.8125Z" fill="url(#paint2_linear_167_1206)" />
                </g>
                <g id="Group 2394">
                  <g id="Rectangle 1154_2" filter="url(#filter2_di_167_1206)">
                    <path d="M237 156.574C238.657 156.574 240 157.917 240 159.574L240 177.133C240 178.789 238.657 180.133 237 180.133L209.08 180.133L209.08 156.574L237 156.574Z" fill="url(#paint3_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_2" d="M235.055 159.52C236.159 159.52 237.055 160.415 237.055 161.52L237.055 175.188C237.055 176.293 236.159 177.188 235.055 177.188L209.079 177.188L209.079 159.52L235.055 159.52Z" fill="url(#paint4_linear_167_1206)" />
                </g>
                <g id="Group 2393_2">
                  <g id="Rectangle 1154_3" filter="url(#filter3_di_167_1206)">
                    <path d="M3 180.133C1.34315 180.133 1.76132e-07 178.79 3.93402e-07 177.133L2.69589e-06 159.575C2.91316e-06 157.918 1.34315 156.575 3 156.575L30.9202 156.575L30.9202 180.133L3 180.133Z" fill="url(#paint5_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_3" d="M4.94531 177.188C3.84074 177.188 2.94531 176.292 2.94531 175.187L2.94531 161.519C2.94531 160.414 3.84075 159.519 4.94531 159.519L30.9208 159.519L30.9208 177.188L4.94531 177.188Z" fill="url(#paint6_linear_167_1206)" />
                </g>
                <g id="Group 2394_2">
                  <g id="Rectangle 1154_4" filter="url(#filter4_di_167_1206)">
                    <path d="M3 84.4258C1.34315 84.4258 1.76132e-07 83.0826 3.93402e-07 81.4258L2.69589e-06 63.8675C2.91316e-06 62.2106 1.34315 60.8675 3 60.8675L30.9202 60.8675L30.9202 84.4258L3 84.4258Z" fill="url(#paint7_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_4" d="M4.94531 81.4805C3.84074 81.4805 2.94531 80.585 2.94531 79.4805L2.94531 65.8118C2.94531 64.7072 3.84075 63.8118 4.94531 63.8118L30.9208 63.8118L30.9208 81.4805L4.94531 81.4805Z" fill="url(#paint8_linear_167_1206)" />
                </g>
                <g id="Group 2393_3">
                  <g id="Rectangle 1154_5" filter="url(#filter5_di_167_1206)">
                    <path d="M60.3682 3.5C60.3682 1.84315 61.7113 0.5 63.3682 0.5L80.9264 0.500001C82.5833 0.500001 83.9264 1.84315 83.9264 3.5L83.9264 31.4202L60.3682 31.4202L60.3682 3.5Z" fill="url(#paint9_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_5" d="M63.3125 5.44531C63.3125 4.34074 64.2079 3.44531 65.3125 3.44531L78.9812 3.44531C80.0858 3.44531 80.9812 4.34074 80.9812 5.44531L80.9812 31.4208L63.3125 31.4208L63.3125 5.44531Z" fill="url(#paint10_linear_167_1206)" />
                </g>
                <g id="Group 2394_3">
                  <g id="Rectangle 1154_6" filter="url(#filter6_di_167_1206)">
                    <path d="M156.073 3.5C156.073 1.84315 157.416 0.5 159.073 0.5L176.632 0.500001C178.288 0.500001 179.632 1.84315 179.632 3.5L179.632 31.4202L156.073 31.4202L156.073 3.5Z" fill="url(#paint11_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_6" d="M159.019 5.44531C159.019 4.34074 159.914 3.44531 161.019 3.44531L174.687 3.44531C175.792 3.44531 176.687 4.34074 176.687 5.44531L176.687 31.4208L159.019 31.4208L159.019 5.44531Z" fill="url(#paint12_linear_167_1206)" />
                </g>
                <g id="Group 2393_4">
                  <g id="Rectangle 1154_7" filter="url(#filter7_di_167_1206)">
                    <path d="M179.632 237.5C179.632 239.157 178.289 240.5 176.632 240.5L159.074 240.5C157.417 240.5 156.074 239.157 156.074 237.5L156.074 209.58L179.632 209.58L179.632 237.5Z" fill="url(#paint13_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_7" d="M176.688 235.555C176.688 236.659 175.792 237.555 174.687 237.555L161.019 237.555C159.914 237.555 159.019 236.659 159.019 235.555L159.019 209.579L176.688 209.579L176.688 235.555Z" fill="url(#paint14_linear_167_1206)" />
                </g>
                <g id="Group 2394_4">
                  <g id="Rectangle 1154_8" filter="url(#filter8_di_167_1206)">
                    <path d="M83.9268 237.5C83.9268 239.157 82.5836 240.5 80.9268 240.5L63.3685 240.5C61.7116 240.5 60.3685 239.157 60.3685 237.5L60.3685 209.58L83.9268 209.58L83.9268 237.5Z" fill="url(#paint15_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_8" d="M80.9814 235.555C80.9814 236.659 80.086 237.555 78.9814 237.555L65.3127 237.555C64.2082 237.555 63.3127 236.659 63.3127 235.555L63.3127 209.579L80.9814 209.579L80.9814 235.555Z" fill="url(#paint16_linear_167_1206)" />
                </g>
                <g id="Group 2460">
                  <g id="Rectangle 1157">
                    <rect
                      x="197.72"
                      y="172.106"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 197.72 172.106)"
                      fill="#C4C4C4"
                    />
                    <rect
                      x="197.72"
                      y="172.106"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 197.72 172.106)"
                      fill="url(#paint17_linear_167_1206)"
                    />
                  </g>
                  <g id="Rectangle 1159" filter="url(#filter9_b_167_1206)">
                    <rect
                      x="198"
                      y="172"
                      width="8.00001"
                      height="155"
                      transform="rotate(90 198 172)"
                      fill="black"
                      fill-opacity="0.01"
                    />
                  </g>
                </g>
                <g id="Group 2461">
                  <g id="Mask Group" filter="url(#filter10_d_167_1206)">
                    <mask
                      id="mask0_167_1206"
                      style="mask-type:alpha"
                      maskUnits="userSpaceOnUse"
                      x="43"
                      y="157"
                      width="155"
                      height="8"
                    >
                      <rect
                        id="Rectangle 1158"
                        x="197.72"
                        y="157.185"
                        width="7.46114"
                        height="154.197"
                        transform="rotate(90 197.72 157.185)"
                        fill="url(#paint18_linear_167_1206)"
                      />
                    </mask>
                    <g mask="url(#mask0_167_1206)">
                      <g id="Rectangle 1159_2" filter="url(#filter11_f_167_1206)">
                        <rect
                          x="202.693"
                          y="157.185"
                          width="7.46114"
                          height="165.389"
                          transform="rotate(90 202.693 157.185)"
                          fill="url(#paint19_linear_167_1206)"
                        />
                      </g>
                    </g>
                  </g>
                  <g id="Rectangle 1158_2" filter="url(#filter12_b_167_1206)">
                    <rect
                      x="198"
                      y="157"
                      width="8.00001"
                      height="155"
                      transform="rotate(90 198 157)"
                      fill="black"
                      fill-opacity="0.01"
                    />
                  </g>
                </g>
                <g id="Group 2462">
                  <g id="Mask Group_2" filter="url(#filter13_d_167_1206)">
                    <mask
                      id="mask1_167_1206"
                      style="mask-type:alpha"
                      maskUnits="userSpaceOnUse"
                      x="43"
                      y="61"
                      width="155"
                      height="8"
                    >
                      <rect
                        id="Rectangle 1158_3"
                        x="197.72"
                        y="61.4326"
                        width="7.46114"
                        height="154.197"
                        transform="rotate(90 197.72 61.4326)"
                        fill="url(#paint20_linear_167_1206)"
                      />
                    </mask>
                    <g mask="url(#mask1_167_1206)">
                      <g id="Rectangle 1159_3" filter="url(#filter14_f_167_1206)">
                        <rect
                          x="202.693"
                          y="61.4326"
                          width="7.46114"
                          height="165.389"
                          transform="rotate(90 202.693 61.4326)"
                          fill="url(#paint21_linear_167_1206)"
                        />
                      </g>
                    </g>
                  </g>
                  <g id="Rectangle 1158_4" filter="url(#filter15_b_167_1206)">
                    <rect
                      x="197.72"
                      y="61.4326"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 197.72 61.4326)"
                      fill="black"
                      fill-opacity="0.01"
                    />
                  </g>
                </g>
                <g id="Group 2463">
                  <g id="Rectangle 1157_2">
                    <rect
                      x="197.72"
                      y="76.3545"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 197.72 76.3545)"
                      fill="#C4C4C4"
                    />
                    <rect
                      x="197.72"
                      y="76.3545"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 197.72 76.3545)"
                      fill="url(#paint22_linear_167_1206)"
                    />
                  </g>
                  <g id="Rectangle 1159_4" filter="url(#filter16_b_167_1206)">
                    <rect
                      x="197.72"
                      y="76.3545"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 197.72 76.3545)"
                      fill="black"
                      fill-opacity="0.01"
                    />
                  </g>
                </g>
                <g class="squareHover" id="light1">
                  <rect
                    id="Rectangle 1161"
                    x="43"
                    y="61"
                    width="155"
                    height="8"
                    fill="url(#paint23_linear_167_1206)"
                  />
                  <g id="Rectangle 1162" filter="url(#filter17_f_167_1206)">
                    <rect x="43" y="61" width="155" height="8" fill="url(#paint24_linear_167_1206)" />
                  </g>
                </g>
                <g class="squareHover" id="light2">
                  <rect
                    id="Rectangle 1161_2"
                    x="43"
                    y="76"
                    width="155"
                    height="8"
                    fill="url(#paint25_linear_167_1206)"
                  />
                  <g id="Rectangle 1162_2" filter="url(#filter18_f_167_1206)">
                    <rect x="43" y="76" width="155" height="8" fill="url(#paint26_linear_167_1206)" />
                  </g>
                </g>
                <g class="squareHover" id="light4">
                  <rect
                    id="Rectangle 1161_3"
                    x="43"
                    y="172"
                    width="155"
                    height="8"
                    fill="url(#paint27_linear_167_1206)"
                  />
                  <g id="Rectangle 1162_3" filter="url(#filter19_f_167_1206)">
                    <rect x="43" y="172" width="155" height="8" fill="url(#paint28_linear_167_1206)" />
                  </g>
                </g>
                <g class="squareHover" id="light3">
                  <rect
                    id="Rectangle 1161_4"
                    x="43"
                    y="157"
                    width="155"
                    height="8"
                    fill="url(#paint29_linear_167_1206)"
                  />
                  <g id="Rectangle 1162_4" filter="url(#filter20_f_167_1206)">
                    <rect x="43" y="157" width="155" height="8" fill="url(#paint30_linear_167_1206)" />
                  </g>
                </g>
              </g>
              <defs>
                <filter
                  id="filter0_di_167_1206"
                  x="-34"
                  y="-33"
                  width="308"
                  height="308"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="32.5" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.5 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="10" dy="10" />
                  <feGaussianBlur stdDeviation="7.5" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter1_di_167_1206"
                  x="205.08"
                  y="56.8672"
                  width="38.9199"
                  height="31.5586"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter2_di_167_1206"
                  x="205.08"
                  y="152.574"
                  width="38.9199"
                  height="31.5586"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter3_di_167_1206"
                  x="-4"
                  y="152.574"
                  width="38.9199"
                  height="31.5586"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter4_di_167_1206"
                  x="-4"
                  y="56.8672"
                  width="38.9199"
                  height="31.5586"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter5_di_167_1206"
                  x="56.3682"
                  y="-3.5"
                  width="31.5586"
                  height="38.9199"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter6_di_167_1206"
                  x="152.073"
                  y="-3.5"
                  width="31.5586"
                  height="38.9199"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter7_di_167_1206"
                  x="152.073"
                  y="205.58"
                  width="31.5586"
                  height="38.9199"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter8_di_167_1206"
                  x="56.3682"
                  y="205.58"
                  width="31.5586"
                  height="38.9199"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter9_b_167_1206"
                  x="40"
                  y="169"
                  width="161"
                  height="14"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feGaussianBlur in="BackgroundImage" stdDeviation="1.5" />
                  <feComposite in2="SourceAlpha" operator="in" result="effect1_backgroundBlur_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_backgroundBlur_167_1206" result="shape" />
                </filter>
                <filter
                  id="filter10_d_167_1206"
                  x="39.5225"
                  y="157.185"
                  width="162.197"
                  height="15.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dy="4" />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                </filter>
                <filter
                  id="filter11_f_167_1206"
                  x="34.3047"
                  y="154.185"
                  width="171.389"
                  height="13.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="1.5" result="effect1_foregroundBlur_167_1206" />
                </filter>
                <filter
                  id="filter12_b_167_1206"
                  x="40"
                  y="154"
                  width="161"
                  height="14"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feGaussianBlur in="BackgroundImage" stdDeviation="1.5" />
                  <feComposite in2="SourceAlpha" operator="in" result="effect1_backgroundBlur_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_backgroundBlur_167_1206" result="shape" />
                </filter>
                <filter
                  id="filter13_d_167_1206"
                  x="39.5225"
                  y="61.4326"
                  width="162.197"
                  height="15.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dy="4" />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                </filter>
                <filter
                  id="filter14_f_167_1206"
                  x="34.3047"
                  y="58.4326"
                  width="171.389"
                  height="13.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="1.5" result="effect1_foregroundBlur_167_1206" />
                </filter>
                <filter
                  id="filter15_b_167_1206"
                  x="40.5225"
                  y="58.4326"
                  width="160.197"
                  height="13.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feGaussianBlur in="BackgroundImage" stdDeviation="1.5" />
                  <feComposite in2="SourceAlpha" operator="in" result="effect1_backgroundBlur_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_backgroundBlur_167_1206" result="shape" />
                </filter>
                <filter
                  id="filter16_b_167_1206"
                  x="40.5225"
                  y="73.3545"
                  width="160.197"
                  height="13.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feGaussianBlur in="BackgroundImage" stdDeviation="1.5" />
                  <feComposite in2="SourceAlpha" operator="in" result="effect1_backgroundBlur_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_backgroundBlur_167_1206" result="shape" />
                </filter>
                <filter
                  id="filter17_f_167_1206"
                  x="28"
                  y="46"
                  width="185"
                  height="38"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="7.5" result="effect1_foregroundBlur_167_1206" />
                </filter>
                <filter
                  id="filter18_f_167_1206"
                  x="28"
                  y="61"
                  width="185"
                  height="38"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="7.5" result="effect1_foregroundBlur_167_1206" />
                </filter>
                <filter
                  id="filter19_f_167_1206"
                  x="28"
                  y="157"
                  width="185"
                  height="38"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="7.5" result="effect1_foregroundBlur_167_1206" />
                </filter>
                <filter
                  id="filter20_f_167_1206"
                  x="28"
                  y="142"
                  width="185"
                  height="38"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="7.5" result="effect1_foregroundBlur_167_1206" />
                </filter>
                <radialGradient
                  id="paint0_radial_167_1206"
                  cx="0"
                  cy="0"
                  r="1"
                  gradientUnits="userSpaceOnUse"
                  gradientTransform="translate(198 51.375) rotate(7.81946) scale(335.35 329.863)"
                >
                  <stop stop-color="#0B0B0D" />
                  <stop offset="1" stop-color="#303338" />
                </radialGradient>
                <linearGradient
                  id="paint1_linear_167_1206"
                  x1="240"
                  y1="72.6463"
                  x2="209.08"
                  y2="72.6463"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint2_linear_167_1206"
                  x1="237.055"
                  y1="72.6469"
                  x2="209.079"
                  y2="72.6469"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint3_linear_167_1206"
                  x1="240"
                  y1="168.353"
                  x2="209.08"
                  y2="168.353"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint4_linear_167_1206"
                  x1="237.055"
                  y1="168.354"
                  x2="209.079"
                  y2="168.354"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint5_linear_167_1206"
                  x1="1.54465e-06"
                  y1="168.354"
                  x2="30.9202"
                  y2="168.354"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint6_linear_167_1206"
                  x1="2.94531"
                  y1="168.353"
                  x2="30.9208"
                  y2="168.353"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint7_linear_167_1206"
                  x1="1.54465e-06"
                  y1="72.6466"
                  x2="30.9202"
                  y2="72.6466"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint8_linear_167_1206"
                  x1="2.94531"
                  y1="72.6461"
                  x2="30.9208"
                  y2="72.6461"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint9_linear_167_1206"
                  x1="72.1473"
                  y1="0.500001"
                  x2="72.1473"
                  y2="31.4202"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint10_linear_167_1206"
                  x1="72.1469"
                  y1="3.44531"
                  x2="72.1469"
                  y2="31.4208"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint11_linear_167_1206"
                  x1="167.852"
                  y1="0.500001"
                  x2="167.852"
                  y2="31.4202"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint12_linear_167_1206"
                  x1="167.853"
                  y1="3.44531"
                  x2="167.853"
                  y2="31.4208"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint13_linear_167_1206"
                  x1="167.853"
                  y1="240.5"
                  x2="167.853"
                  y2="209.58"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint14_linear_167_1206"
                  x1="167.853"
                  y1="237.555"
                  x2="167.853"
                  y2="209.579"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint15_linear_167_1206"
                  x1="72.1476"
                  y1="240.5"
                  x2="72.1476"
                  y2="209.58"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint16_linear_167_1206"
                  x1="72.1471"
                  y1="237.555"
                  x2="72.1471"
                  y2="209.579"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint17_linear_167_1206"
                  x1="205.181"
                  y1="223.713"
                  x2="197.72"
                  y2="223.713"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint18_linear_167_1206"
                  x1="205.181"
                  y1="208.791"
                  x2="197.72"
                  y2="208.791"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint19_linear_167_1206"
                  x1="210.154"
                  y1="212.536"
                  x2="202.693"
                  y2="212.536"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint20_linear_167_1206"
                  x1="205.181"
                  y1="113.039"
                  x2="197.72"
                  y2="113.039"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint21_linear_167_1206"
                  x1="210.154"
                  y1="116.784"
                  x2="202.693"
                  y2="116.784"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint22_linear_167_1206"
                  x1="205.181"
                  y1="127.961"
                  x2="197.72"
                  y2="127.961"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint23_linear_167_1206"
                  x1="61.6201"
                  y1="61"
                  x2="61.6201"
                  y2="69"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint24_linear_167_1206"
                  x1="61.6201"
                  y1="61"
                  x2="61.6201"
                  y2="69"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint25_linear_167_1206"
                  x1="61.6201"
                  y1="76"
                  x2="61.6201"
                  y2="84"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint26_linear_167_1206"
                  x1="61.6201"
                  y1="76"
                  x2="61.6201"
                  y2="84"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint27_linear_167_1206"
                  x1="61.6201"
                  y1="172"
                  x2="61.6201"
                  y2="180"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint28_linear_167_1206"
                  x1="61.6201"
                  y1="172"
                  x2="61.6201"
                  y2="180"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint29_linear_167_1206"
                  x1="61.6201"
                  y1="157"
                  x2="61.6201"
                  y2="165"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint30_linear_167_1206"
                  x1="61.6201"
                  y1="157"
                  x2="61.6201"
                  y2="165"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
              </defs>
            </svg>
            <p>
              {{ datablock5.square_text[1] }}
            </p>
          </div>
          <div class="mainPage_block5_anim_square s3">
            <svg viewBox="0 0 240 241">
              <g id="Group 2412">
                <g id="Group 2465">
                  <g id="Rectangle 1153" filter="url(#filter0_di_167_1206)">
                    <rect
                      x="209"
                      y="32"
                      width="178"
                      height="178"
                      transform="rotate(90 209 32)"
                      fill="#0D0F13"
                    />
                  </g>
                  <rect
                    id="Rectangle 1156"
                    x="198"
                    y="47"
                    width="150"
                    height="155"
                    transform="rotate(90 198 47)"
                    fill="url(#paint0_radial_167_1206)"
                  />
                </g>
                <g id="Group 2393">
                  <g id="Rectangle 1154" filter="url(#filter1_di_167_1206)">
                    <path d="M237 60.8672C238.657 60.8672 240 62.2103 240 63.8672L240 81.4255C240 83.0823 238.657 84.4255 237 84.4255L209.08 84.4255L209.08 60.8672L237 60.8672Z" fill="url(#paint1_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155" d="M235.055 63.8125C236.159 63.8125 237.055 64.7079 237.055 65.8125L237.055 79.4812C237.055 80.5858 236.159 81.4812 235.055 81.4812L209.079 81.4812L209.079 63.8125L235.055 63.8125Z" fill="url(#paint2_linear_167_1206)" />
                </g>
                <g id="Group 2394">
                  <g id="Rectangle 1154_2" filter="url(#filter2_di_167_1206)">
                    <path d="M237 156.574C238.657 156.574 240 157.917 240 159.574L240 177.133C240 178.789 238.657 180.133 237 180.133L209.08 180.133L209.08 156.574L237 156.574Z" fill="url(#paint3_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_2" d="M235.055 159.52C236.159 159.52 237.055 160.415 237.055 161.52L237.055 175.188C237.055 176.293 236.159 177.188 235.055 177.188L209.079 177.188L209.079 159.52L235.055 159.52Z" fill="url(#paint4_linear_167_1206)" />
                </g>
                <g id="Group 2393_2">
                  <g id="Rectangle 1154_3" filter="url(#filter3_di_167_1206)">
                    <path d="M3 180.133C1.34315 180.133 1.76132e-07 178.79 3.93402e-07 177.133L2.69589e-06 159.575C2.91316e-06 157.918 1.34315 156.575 3 156.575L30.9202 156.575L30.9202 180.133L3 180.133Z" fill="url(#paint5_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_3" d="M4.94531 177.188C3.84074 177.188 2.94531 176.292 2.94531 175.187L2.94531 161.519C2.94531 160.414 3.84075 159.519 4.94531 159.519L30.9208 159.519L30.9208 177.188L4.94531 177.188Z" fill="url(#paint6_linear_167_1206)" />
                </g>
                <g id="Group 2394_2">
                  <g id="Rectangle 1154_4" filter="url(#filter4_di_167_1206)">
                    <path d="M3 84.4258C1.34315 84.4258 1.76132e-07 83.0826 3.93402e-07 81.4258L2.69589e-06 63.8675C2.91316e-06 62.2106 1.34315 60.8675 3 60.8675L30.9202 60.8675L30.9202 84.4258L3 84.4258Z" fill="url(#paint7_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_4" d="M4.94531 81.4805C3.84074 81.4805 2.94531 80.585 2.94531 79.4805L2.94531 65.8118C2.94531 64.7072 3.84075 63.8118 4.94531 63.8118L30.9208 63.8118L30.9208 81.4805L4.94531 81.4805Z" fill="url(#paint8_linear_167_1206)" />
                </g>
                <g id="Group 2393_3">
                  <g id="Rectangle 1154_5" filter="url(#filter5_di_167_1206)">
                    <path d="M60.3682 3.5C60.3682 1.84315 61.7113 0.5 63.3682 0.5L80.9264 0.500001C82.5833 0.500001 83.9264 1.84315 83.9264 3.5L83.9264 31.4202L60.3682 31.4202L60.3682 3.5Z" fill="url(#paint9_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_5" d="M63.3125 5.44531C63.3125 4.34074 64.2079 3.44531 65.3125 3.44531L78.9812 3.44531C80.0858 3.44531 80.9812 4.34074 80.9812 5.44531L80.9812 31.4208L63.3125 31.4208L63.3125 5.44531Z" fill="url(#paint10_linear_167_1206)" />
                </g>
                <g id="Group 2394_3">
                  <g id="Rectangle 1154_6" filter="url(#filter6_di_167_1206)">
                    <path d="M156.073 3.5C156.073 1.84315 157.416 0.5 159.073 0.5L176.632 0.500001C178.288 0.500001 179.632 1.84315 179.632 3.5L179.632 31.4202L156.073 31.4202L156.073 3.5Z" fill="url(#paint11_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_6" d="M159.019 5.44531C159.019 4.34074 159.914 3.44531 161.019 3.44531L174.687 3.44531C175.792 3.44531 176.687 4.34074 176.687 5.44531L176.687 31.4208L159.019 31.4208L159.019 5.44531Z" fill="url(#paint12_linear_167_1206)" />
                </g>
                <g id="Group 2393_4">
                  <g id="Rectangle 1154_7" filter="url(#filter7_di_167_1206)">
                    <path d="M179.632 237.5C179.632 239.157 178.289 240.5 176.632 240.5L159.074 240.5C157.417 240.5 156.074 239.157 156.074 237.5L156.074 209.58L179.632 209.58L179.632 237.5Z" fill="url(#paint13_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_7" d="M176.688 235.555C176.688 236.659 175.792 237.555 174.687 237.555L161.019 237.555C159.914 237.555 159.019 236.659 159.019 235.555L159.019 209.579L176.688 209.579L176.688 235.555Z" fill="url(#paint14_linear_167_1206)" />
                </g>
                <g id="Group 2394_4">
                  <g id="Rectangle 1154_8" filter="url(#filter8_di_167_1206)">
                    <path d="M83.9268 237.5C83.9268 239.157 82.5836 240.5 80.9268 240.5L63.3685 240.5C61.7116 240.5 60.3685 239.157 60.3685 237.5L60.3685 209.58L83.9268 209.58L83.9268 237.5Z" fill="url(#paint15_linear_167_1206)" />
                  </g>
                  <path id="Rectangle 1155_8" d="M80.9814 235.555C80.9814 236.659 80.086 237.555 78.9814 237.555L65.3127 237.555C64.2082 237.555 63.3127 236.659 63.3127 235.555L63.3127 209.579L80.9814 209.579L80.9814 235.555Z" fill="url(#paint16_linear_167_1206)" />
                </g>
                <g id="Group 2460">
                  <g id="Rectangle 1157">
                    <rect
                      x="197.72"
                      y="172.106"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 197.72 172.106)"
                      fill="#C4C4C4"
                    />
                    <rect
                      x="197.72"
                      y="172.106"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 197.72 172.106)"
                      fill="url(#paint17_linear_167_1206)"
                    />
                  </g>
                  <g id="Rectangle 1159" filter="url(#filter9_b_167_1206)">
                    <rect
                      x="198"
                      y="172"
                      width="8.00001"
                      height="155"
                      transform="rotate(90 198 172)"
                      fill="black"
                      fill-opacity="0.01"
                    />
                  </g>
                </g>
                <g id="Group 2461">
                  <g id="Mask Group" filter="url(#filter10_d_167_1206)">
                    <mask
                      id="mask0_167_1206"
                      style="mask-type:alpha"
                      maskUnits="userSpaceOnUse"
                      x="43"
                      y="157"
                      width="155"
                      height="8"
                    >
                      <rect
                        id="Rectangle 1158"
                        x="197.72"
                        y="157.185"
                        width="7.46114"
                        height="154.197"
                        transform="rotate(90 197.72 157.185)"
                        fill="url(#paint18_linear_167_1206)"
                      />
                    </mask>
                    <g mask="url(#mask0_167_1206)">
                      <g id="Rectangle 1159_2" filter="url(#filter11_f_167_1206)">
                        <rect
                          x="202.693"
                          y="157.185"
                          width="7.46114"
                          height="165.389"
                          transform="rotate(90 202.693 157.185)"
                          fill="url(#paint19_linear_167_1206)"
                        />
                      </g>
                    </g>
                  </g>
                  <g id="Rectangle 1158_2" filter="url(#filter12_b_167_1206)">
                    <rect
                      x="198"
                      y="157"
                      width="8.00001"
                      height="155"
                      transform="rotate(90 198 157)"
                      fill="black"
                      fill-opacity="0.01"
                    />
                  </g>
                </g>
                <g id="Group 2462">
                  <g id="Mask Group_2" filter="url(#filter13_d_167_1206)">
                    <mask
                      id="mask1_167_1206"
                      style="mask-type:alpha"
                      maskUnits="userSpaceOnUse"
                      x="43"
                      y="61"
                      width="155"
                      height="8"
                    >
                      <rect
                        id="Rectangle 1158_3"
                        x="197.72"
                        y="61.4326"
                        width="7.46114"
                        height="154.197"
                        transform="rotate(90 197.72 61.4326)"
                        fill="url(#paint20_linear_167_1206)"
                      />
                    </mask>
                    <g mask="url(#mask1_167_1206)">
                      <g id="Rectangle 1159_3" filter="url(#filter14_f_167_1206)">
                        <rect
                          x="202.693"
                          y="61.4326"
                          width="7.46114"
                          height="165.389"
                          transform="rotate(90 202.693 61.4326)"
                          fill="url(#paint21_linear_167_1206)"
                        />
                      </g>
                    </g>
                  </g>
                  <g id="Rectangle 1158_4" filter="url(#filter15_b_167_1206)">
                    <rect
                      x="197.72"
                      y="61.4326"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 197.72 61.4326)"
                      fill="black"
                      fill-opacity="0.01"
                    />
                  </g>
                </g>
                <g id="Group 2463">
                  <g id="Rectangle 1157_2">
                    <rect
                      x="197.72"
                      y="76.3545"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 197.72 76.3545)"
                      fill="#C4C4C4"
                    />
                    <rect
                      x="197.72"
                      y="76.3545"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 197.72 76.3545)"
                      fill="url(#paint22_linear_167_1206)"
                    />
                  </g>
                  <g id="Rectangle 1159_4" filter="url(#filter16_b_167_1206)">
                    <rect
                      x="197.72"
                      y="76.3545"
                      width="7.46114"
                      height="154.197"
                      transform="rotate(90 197.72 76.3545)"
                      fill="black"
                      fill-opacity="0.01"
                    />
                  </g>
                </g>
                <g class="squareHover" id="light1">
                  <rect
                    id="Rectangle 1161"
                    x="43"
                    y="61"
                    width="155"
                    height="8"
                    fill="url(#paint23_linear_167_1206)"
                  />
                  <g id="Rectangle 1162" filter="url(#filter17_f_167_1206)">
                    <rect x="43" y="61" width="155" height="8" fill="url(#paint24_linear_167_1206)" />
                  </g>
                </g>
                <g class="squareHover" id="light2">
                  <rect
                    id="Rectangle 1161_2"
                    x="43"
                    y="76"
                    width="155"
                    height="8"
                    fill="url(#paint25_linear_167_1206)"
                  />
                  <g id="Rectangle 1162_2" filter="url(#filter18_f_167_1206)">
                    <rect x="43" y="76" width="155" height="8" fill="url(#paint26_linear_167_1206)" />
                  </g>
                </g>
                <g class="squareHover" id="light4">
                  <rect
                    id="Rectangle 1161_3"
                    x="43"
                    y="172"
                    width="155"
                    height="8"
                    fill="url(#paint27_linear_167_1206)"
                  />
                  <g id="Rectangle 1162_3" filter="url(#filter19_f_167_1206)">
                    <rect x="43" y="172" width="155" height="8" fill="url(#paint28_linear_167_1206)" />
                  </g>
                </g>
                <g class="squareHover" id="light3">
                  <rect
                    id="Rectangle 1161_4"
                    x="43"
                    y="157"
                    width="155"
                    height="8"
                    fill="url(#paint29_linear_167_1206)"
                  />
                  <g id="Rectangle 1162_4" filter="url(#filter20_f_167_1206)">
                    <rect x="43" y="157" width="155" height="8" fill="url(#paint30_linear_167_1206)" />
                  </g>
                </g>
              </g>
              <defs>
                <filter
                  id="filter0_di_167_1206"
                  x="-34"
                  y="-33"
                  width="308"
                  height="308"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="32.5" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.5 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="10" dy="10" />
                  <feGaussianBlur stdDeviation="7.5" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter1_di_167_1206"
                  x="205.08"
                  y="56.8672"
                  width="38.9199"
                  height="31.5586"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter2_di_167_1206"
                  x="205.08"
                  y="152.574"
                  width="38.9199"
                  height="31.5586"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter3_di_167_1206"
                  x="-4"
                  y="152.574"
                  width="38.9199"
                  height="31.5586"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter4_di_167_1206"
                  x="-4"
                  y="56.8672"
                  width="38.9199"
                  height="31.5586"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter5_di_167_1206"
                  x="56.3682"
                  y="-3.5"
                  width="31.5586"
                  height="38.9199"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter6_di_167_1206"
                  x="152.073"
                  y="-3.5"
                  width="31.5586"
                  height="38.9199"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter7_di_167_1206"
                  x="152.073"
                  y="205.58"
                  width="31.5586"
                  height="38.9199"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter8_di_167_1206"
                  x="56.3682"
                  y="205.58"
                  width="31.5586"
                  height="38.9199"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.45 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dx="4" />
                  <feGaussianBlur stdDeviation="1" />
                  <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0.291667 0 0 0 0 0.268576 0 0 0 0 0.268576 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="shape" result="effect2_innerShadow_167_1206" />
                </filter>
                <filter
                  id="filter9_b_167_1206"
                  x="40"
                  y="169"
                  width="161"
                  height="14"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feGaussianBlur in="BackgroundImage" stdDeviation="1.5" />
                  <feComposite in2="SourceAlpha" operator="in" result="effect1_backgroundBlur_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_backgroundBlur_167_1206" result="shape" />
                </filter>
                <filter
                  id="filter10_d_167_1206"
                  x="39.5225"
                  y="157.185"
                  width="162.197"
                  height="15.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dy="4" />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                </filter>
                <filter
                  id="filter11_f_167_1206"
                  x="34.3047"
                  y="154.185"
                  width="171.389"
                  height="13.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="1.5" result="effect1_foregroundBlur_167_1206" />
                </filter>
                <filter
                  id="filter12_b_167_1206"
                  x="40"
                  y="154"
                  width="161"
                  height="14"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feGaussianBlur in="BackgroundImage" stdDeviation="1.5" />
                  <feComposite in2="SourceAlpha" operator="in" result="effect1_backgroundBlur_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_backgroundBlur_167_1206" result="shape" />
                </filter>
                <filter
                  id="filter13_d_167_1206"
                  x="39.5225"
                  y="61.4326"
                  width="162.197"
                  height="15.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha" />
                  <feOffset dy="4" />
                  <feGaussianBlur stdDeviation="2" />
                  <feComposite in2="hardAlpha" operator="out" />
                  <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0" />
                  <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_167_1206" result="shape" />
                </filter>
                <filter
                  id="filter14_f_167_1206"
                  x="34.3047"
                  y="58.4326"
                  width="171.389"
                  height="13.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="1.5" result="effect1_foregroundBlur_167_1206" />
                </filter>
                <filter
                  id="filter15_b_167_1206"
                  x="40.5225"
                  y="58.4326"
                  width="160.197"
                  height="13.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feGaussianBlur in="BackgroundImage" stdDeviation="1.5" />
                  <feComposite in2="SourceAlpha" operator="in" result="effect1_backgroundBlur_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_backgroundBlur_167_1206" result="shape" />
                </filter>
                <filter
                  id="filter16_b_167_1206"
                  x="40.5225"
                  y="73.3545"
                  width="160.197"
                  height="13.4609"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feGaussianBlur in="BackgroundImage" stdDeviation="1.5" />
                  <feComposite in2="SourceAlpha" operator="in" result="effect1_backgroundBlur_167_1206" />
                  <feBlend mode="normal" in="SourceGraphic" in2="effect1_backgroundBlur_167_1206" result="shape" />
                </filter>
                <filter
                  id="filter17_f_167_1206"
                  x="28"
                  y="46"
                  width="185"
                  height="38"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="7.5" result="effect1_foregroundBlur_167_1206" />
                </filter>
                <filter
                  id="filter18_f_167_1206"
                  x="28"
                  y="61"
                  width="185"
                  height="38"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="7.5" result="effect1_foregroundBlur_167_1206" />
                </filter>
                <filter
                  id="filter19_f_167_1206"
                  x="28"
                  y="157"
                  width="185"
                  height="38"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="7.5" result="effect1_foregroundBlur_167_1206" />
                </filter>
                <filter
                  id="filter20_f_167_1206"
                  x="28"
                  y="142"
                  width="185"
                  height="38"
                  filterUnits="userSpaceOnUse"
                  color-interpolation-filters="sRGB"
                >
                  <feFlood flood-opacity="0" result="BackgroundImageFix" />
                  <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape" />
                  <feGaussianBlur stdDeviation="7.5" result="effect1_foregroundBlur_167_1206" />
                </filter>
                <radialGradient
                  id="paint0_radial_167_1206"
                  cx="0"
                  cy="0"
                  r="1"
                  gradientUnits="userSpaceOnUse"
                  gradientTransform="translate(198 51.375) rotate(7.81946) scale(335.35 329.863)"
                >
                  <stop stop-color="#0B0B0D" />
                  <stop offset="1" stop-color="#303338" />
                </radialGradient>
                <linearGradient
                  id="paint1_linear_167_1206"
                  x1="240"
                  y1="72.6463"
                  x2="209.08"
                  y2="72.6463"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint2_linear_167_1206"
                  x1="237.055"
                  y1="72.6469"
                  x2="209.079"
                  y2="72.6469"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint3_linear_167_1206"
                  x1="240"
                  y1="168.353"
                  x2="209.08"
                  y2="168.353"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint4_linear_167_1206"
                  x1="237.055"
                  y1="168.354"
                  x2="209.079"
                  y2="168.354"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint5_linear_167_1206"
                  x1="1.54465e-06"
                  y1="168.354"
                  x2="30.9202"
                  y2="168.354"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint6_linear_167_1206"
                  x1="2.94531"
                  y1="168.353"
                  x2="30.9208"
                  y2="168.353"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint7_linear_167_1206"
                  x1="1.54465e-06"
                  y1="72.6466"
                  x2="30.9202"
                  y2="72.6466"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint8_linear_167_1206"
                  x1="2.94531"
                  y1="72.6461"
                  x2="30.9208"
                  y2="72.6461"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint9_linear_167_1206"
                  x1="72.1473"
                  y1="0.500001"
                  x2="72.1473"
                  y2="31.4202"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint10_linear_167_1206"
                  x1="72.1469"
                  y1="3.44531"
                  x2="72.1469"
                  y2="31.4208"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint11_linear_167_1206"
                  x1="167.852"
                  y1="0.500001"
                  x2="167.852"
                  y2="31.4202"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint12_linear_167_1206"
                  x1="167.853"
                  y1="3.44531"
                  x2="167.853"
                  y2="31.4208"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint13_linear_167_1206"
                  x1="167.853"
                  y1="240.5"
                  x2="167.853"
                  y2="209.58"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint14_linear_167_1206"
                  x1="167.853"
                  y1="237.555"
                  x2="167.853"
                  y2="209.579"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint15_linear_167_1206"
                  x1="72.1476"
                  y1="240.5"
                  x2="72.1476"
                  y2="209.58"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#25282F" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint16_linear_167_1206"
                  x1="72.1471"
                  y1="237.555"
                  x2="72.1471"
                  y2="209.579"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#303338" />
                  <stop offset="1" stop-color="#0B0B0D" />
                </linearGradient>
                <linearGradient
                  id="paint17_linear_167_1206"
                  x1="205.181"
                  y1="223.713"
                  x2="197.72"
                  y2="223.713"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint18_linear_167_1206"
                  x1="205.181"
                  y1="208.791"
                  x2="197.72"
                  y2="208.791"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint19_linear_167_1206"
                  x1="210.154"
                  y1="212.536"
                  x2="202.693"
                  y2="212.536"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint20_linear_167_1206"
                  x1="205.181"
                  y1="113.039"
                  x2="197.72"
                  y2="113.039"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint21_linear_167_1206"
                  x1="210.154"
                  y1="116.784"
                  x2="202.693"
                  y2="116.784"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint22_linear_167_1206"
                  x1="205.181"
                  y1="127.961"
                  x2="197.72"
                  y2="127.961"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#0D0D10" />
                  <stop offset="0.359375" stop-color="#31313B" />
                  <stop offset="0.65625" stop-color="white" />
                  <stop offset="0.723958" stop-color="#565658" />
                  <stop offset="1" stop-color="#16171A" />
                </linearGradient>
                <linearGradient
                  id="paint23_linear_167_1206"
                  x1="61.6201"
                  y1="61"
                  x2="61.6201"
                  y2="69"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint24_linear_167_1206"
                  x1="61.6201"
                  y1="61"
                  x2="61.6201"
                  y2="69"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint25_linear_167_1206"
                  x1="61.6201"
                  y1="76"
                  x2="61.6201"
                  y2="84"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint26_linear_167_1206"
                  x1="61.6201"
                  y1="76"
                  x2="61.6201"
                  y2="84"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint27_linear_167_1206"
                  x1="61.6201"
                  y1="172"
                  x2="61.6201"
                  y2="180"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint28_linear_167_1206"
                  x1="61.6201"
                  y1="172"
                  x2="61.6201"
                  y2="180"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint29_linear_167_1206"
                  x1="61.6201"
                  y1="157"
                  x2="61.6201"
                  y2="165"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
                <linearGradient
                  id="paint30_linear_167_1206"
                  x1="61.6201"
                  y1="157"
                  x2="61.6201"
                  y2="165"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.186755" stop-color="#1097BB" />
                  <stop offset="0.504464" stop-color="#00FFE0" />
                  <stop offset="0.79613" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#1F4379" />
                </linearGradient>
              </defs>
            </svg>
            <p>
              {{ datablock5.square_text[2] }}
            </p>
          </div> -->
          <a id="block5_btn" class="mainPage_block5_anim_btn btn_blue">{{ datablock5.btn_text }}</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  buildModules: ['nuxt-animejs'],
  name: 'IndexPage',
  filters: {
    addComma (val) {
      return val.toLocaleString()
    }
  },
  layout: 'error',
  // components: {
  //   formCard: () => import('~/components/card')
  // },
  data () {
    return {
      datablock1:
      {
        title: 'Различные инвестиционные портфели: Недвижимость Фармацевтика,  IT-технологии',
        text: 'Определите вашу инвестиционную цель и инвестируйте без рисков.Простой способ долгосрочного инвестирования в готовые решения от нашего фонда.',
        btn_text: 'Читать дальше'
      },
      datablock2:
      {
        title: 'Мгновенный доступ ко всем вариантам заработка на мировых финансовых рынках',
        text: 'Вместе с нами вы сможете инвестировать в IT-технологии, недвижимость и крупнейшие мировые компании. А также торговать криптовалютами, покупать/продавать сырьевые товары или спекулировать различными валютами и активами.'
      },
      datablock3:
      {
        items: [
          {
            id: 1,
            title: 'Начало',
            text: 'История фонда берет свое начало с того момента, когда трейдеры и экономисты решили создать свою финансовую экосистему, которая даст возможность зарабатывать простым людям. Целью этого проекта было развитие и внедрение систем комплексного инвестирования для упрощения работы с инвестициями и торговли на финансовых рынках.'
          },
          {
            id: 2,
            title: 'Детализация',
            text: 'Фонд работает в нескольких направлениях инвестирования: /r -в фармацевтику, /r -в недвижимость, /r -в IT-технологии, /r -в криптовалюты,-в онлайн торговлю. /r  /r Для удобства наших клиентов мы предоставляем различые вариации и условия работы с инвестиционными портфелями. Онлайн трейдинг регулируется соотсвенным законодательством регулятора “этой страны.” '
          },
          {
            id: 3,
            title: 'Развитие',
            text: 'Большие обороты холдинг смог набрать после внедрения возможности получения пассивного дохода без необходимости торговать. Любой клиент может выбрать подходящий ему вариант и зарабатывать стабильный доход на проверенных портфелях фонда. Вы сами выбираете сроки инвестирования и риски, на которые вы готовы пойти.'
          },
          {
            id: 4,
            title: 'Продвижение',
            text: 'Для частных инвесторов портфели будут прибыльным инструментом пассивного дохода. Мы ведем прозрачную работу, при которой наши эксперты выбирают самые выгодные варианты инвестирования в различных сферах. За счет того, что холдинг работает с большими объемами - для инвестора снижается риск, ведь его средства инвестируются в сотни или тысячи ценных бумаг или других активов.  /r  /r Для активных трейдеров, мы можем выделить удобство нашего терминала и возможность совмещения счетов с пассивными и активными доходами. Мы получаем котировки напрямую от ведущих европейских банков, что позволяет существенно улучшить качество работы с нашей платформой. '
          }
        ]
      },
      datablock4:
      {
        isAfterEnable: false,
        items: [
          {
            id: 0,
            value: 3754,
            count: 0,
            text: 'подписанных контрактов за последний месяц'
          },
          {
            id: 1,
            symbol: '$',
            value: 13681062,
            count: 0,
            text: 'объем выходящих транзакций'
          },
          {
            id: 2,
            value: 17780641,
            count: 0,
            text: 'заключено сделок на платформе'
          }
        ]
      },
      datablock5:
      {
        head_text:
        {
          line1: 'InteractiveFund не взимает никаких дополнительных комисcий на ввод/вывод средств.',
          line2: 'Пополняйте и выводите без ограничений'
        },
        btn_text: 'Присоединиться',
        squares: [
          {
            id: 0,
            text: 'Оперативный вывод средств'
          },
          {
            id: 1,
            text: 'Без комиссий '
          },
          {
            id: 2,
            text: 'Без ограничений'
          }
        ]
      }
    }
  },
  computed: {
  },
  watch: {
    id (value) {
      // console.log(value)
    },
    customer: {
      deep: true,
      handler (obj) {
        // console.log(obj)
      }
    }
  },
  created () {
    this.$dark = false
  },
  mounted () {
    window.addEventListener('scroll', this.block4ScrollEvent)
  },
  beforeDestroy () {
    window.removeEventListener('scroll', this.block4ScrollEvent)
  },
  methods: {
    block4ScrollEvent (event) {
      const position = document.querySelector('#block4')
      if ((position.getBoundingClientRect().top <= 300) && (this.datablock4.items[0].count === 0)) {
        this.datablock4.isAfterEnable = true
        this.datablock4.items.forEach((item) => {
          const obj = { n: item.count }
          this.$anime({
            targets: obj,
            n: item.value,
            round: 1,
            duration: 700,
            easing: 'easeInOutSine',
            update: () => {
              item.count = obj.n
            }
          })
        })
      }
    },
    block5Rotate () {
      this.$anime({
        targets: ['.s1', '.s3'],
        translateY: '50%',
        duration: 0
      })
      this.$anime({
        targets: '.s2',
        translateX: '-50%',
        translateY: '-50%',
        duration: 0
      })
      this.$anime({
        targets: ['.s1', '.s2', '.s3'],
        duration: 700,
        rotate: '1turn',
        easing: 'easeInOutSine'
      })
      this.$anime({
        targets: '.mainPage_block5_anim',
        duration: 700,
        height: 500,
        delay: 1000,
        easing: 'linear'
      })
      // this.$anime({
      //   targets: '.mainPage_block5_anim_btn',
      //   display: 'block',
      //   // opacity: 0,
      //   delay: 1000
      // })
      this.$anime({
        targets: '.mainPage_block5_anim_btn',
        duration: 700,
        opacity: 1,
        delay: 1000,
        easing: 'linear'
      })
      this.$anime({
        targets: '.mainPage_block5',
        marginBottom: 200,
        duration: 700,
        delay: 1000,
        easing: 'linear'
      })
      setTimeout(() => {
        document.getElementById('block5_btn').style.display = 'block'
      }, 1000)
    }
  }
}
</script>

<style scoped lang="scss">

@import url('~/assets/scss/abstracts/_placeholders.scss');
@import url('~/assets/scss/abstracts/_variables.scss');
.mainPage{
  &_block1{
    padding: 30px;
    border-radius: 40px;
    position: relative;
    &>video{
      width: 100%;
      border-radius: 40px;
    }
    &_description{
      position: absolute;
      right: 137/1840*100%;
      top: 400/1022*100%;
      max-width: 666/1840*100%;
        font-size: $h6FS !important;
      .title{
        font-size: $h4FS !important;
        line-height: 1.25;
      }
      >a{
        color: $textColor1;
        transition: color $transition_time $transition_anim_type;
        &:hover{
            color: $btncolor1;
        }
      }
    }
  }
  &_block2{
    padding: 30px 70px;
    .text{
      text-align: center;
      font-family: 'Raleway', sans-serif;
      margin: 0 auto 48/1920*100vw;

      max-width: 1620/1920*100vw;
    }
    .title{
      max-width: 1620/1920*100vw;
      text-align: center;
      font-family: 'Manrope', sans-serif;
      margin: 0 auto 48/1920*100vw;
      font-size: $h4FS;
      font-weight: 800;
      line-height: 1;
      letter-spacing: 0.05em;
    }

  }
  &_block3{
    @include makeitflex(row,flex-start);
    background-size: contain;
    &_col{
      @include makeitflex(column,flex-start);
      border-top: 4px #14161B solid ;
      overflow: hidden;
      background-size:contain;
    }
    &_item{
      flex:auto;
      z-index: 1;
      position: relative;
      border-bottom: 4px #14161B solid ;
      transition: display $transition_time !important ;
      filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
      &::after{
        opacity: 0;
        transition: opacity $transition_time linear !important ;
        filter: blur(64px);
        position: absolute;
        left: 0;
        top: 0;
        width: 100%;
        height: 100%;
        z-index: -1;
        content: '';
      }
      &:hover::after{
        opacity: 1;
      }
      & .title{
        font-weight: 600;
        font-size: $h4FS !important;
        margin-bottom: $h6FS;
        z-index: 10;
      }
      & .text{
        font-weight: 300;
        font-size: $h6FS;
        z-index: 10;
      }
    }

    .dataBlock3{
      &_b1::after{
        background: linear-gradient(315deg, rgba(22, 25, 32, 0) 62.32%, #1E232E 69.95%, rgba(34, 53, 111, 0.56) 77.2%, rgba(16, 151, 187, 0.61) 88.43%, rgba(0, 255, 224, 0.92) 94.54%, rgba(0, 255, 224, 0.53) 97.75%);
      }
      &_b2::after{
        background: linear-gradient(142deg, rgba(22, 25, 32, 0) 54.13%, rgba(30, 35, 46, 0.58) 64.18%, rgba(34, 53, 111, 0.6) 71.44%, rgba(16, 151, 187, 0.68) 80.68%, rgba(11, 182, 198, 0.774518) 83.61%, #00FFE0 90.59%);
      }
      &_b3::after{
        background: linear-gradient(15deg, rgba(22, 25, 32, 0) 54.43%, #1E232E 71.89%, rgba(34, 53, 111, 0.56) 82.42%, rgba(16, 151, 187, 0.61) 89%, rgba(0, 255, 224, 0.92) 97.09%, rgba(0, 255, 224, 0.53) 101.34%);
      }
      &_b4::after{
        background-image: linear-gradient(204.67deg, rgba(22, 25, 32, 0) 41.66%, #1E232E 59.64%, rgba(34, 53, 111, 0.56) 70.48%, rgba(16, 151, 187, 0.61) 77.26%, rgba(0, 255, 224, 0.92) 85.59%, rgba(0, 255, 224, 0.53) 89.96%);
      }
    }
    .wide {
      min-width:1125.5/1920*100%;
      border-right: 4px #14161B solid ;
      background-image: url('~/assets/images/pages/Main/block3/col1.svg');
      & .mainPage_block3_item{
        padding: 50px 118px;
      }
    }
    .tall {
      min-width: 617/1920*100%;
      border-left: 4px #14161B solid ;
      background-image: url('~/assets/images/pages/Main/block3/col3.svg');
      & .mainPage_block3_item{
        padding: 40px 30px;
      }
    }
    .middle{
      width:100%;
      border-bottom: 4px #14161B solid ;
      background-image: url('~/assets/images/pages/Main/block3/col2.svg');
      background-size: cover;
      background-position-y: bottom;
    }
  }
  &_block4{
    @include makeitflex(row, space-between);
    background-image: url('~/assets/images/pages/Main/block4/background.svg');
    background-size: contain;
    height: 584px;
    width: 100%;
    margin-bottom: 80px;
    padding: 307px 200px 0;
    position: relative;
    z-index: 1;
    overflow: hidden;
    &.afterEnable{
      &::after{
          opacity:1;
      }
    }
    &::after{
      opacity: 0;
      transition: opacity $transition_time linear !important ;
      position: absolute;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      z-index: -1;
      content: '';
      background: linear-gradient(4deg, rgba(22, 25, 32, 0) 37.9%, rgba(30, 35, 46, 0.58) 52.31%, rgba(34, 53, 111, 0.6) 62.74%, rgba(16, 151, 187, 0.68) 76.01%, #00FFE0 90.22%);
      filter: blur(64px);
    }
    &_item{
      text-align: center;
      flex:1;
      height: fit-content;
      .title{
        font-weight: bold;
        font-size: $h1FS !important ;
        line-height: 87/64*1;
        font-feature-settings: 'pnum' on, 'lnum' on;
      }
      .text{
        font-weight: 500;
        font-size: $h5FS;
        line-height: 33/24*1;
        font-feature-settings: 'pnum' on, 'lnum' on;
        max-width: 67%;
        margin: 0 auto;
      }
    }
  }

  &_block5{
    text-align: center;
    margin-bottom: 400px;
    &.text{
      font-weight: 500;
      font-size: $h7FS;
    };
    &.title{
      font-weight: 800;
      font-size: $h2FS;
    };
    &_anim{
      @include makeitflex(column, center);
      margin-top: 130px;
      background-image: url('~/assets/images/pages/Main/block5/background1.svg');
      background-size: cover;
      background-position-y: top;
      background-position-x: center;
      position: relative;
      height: 0px;
      border-top: black 1px solid;
      &_square{
        cursor: pointer;
        position: absolute;
        width: 240/1920*100vw;
        height: 240/1920*100vw;
        font-weight: 600;
        font-size: $h7FS;
        line-height: 135%;
        text-align: center;
        text-align: center;
        letter-spacing: 0.05em;
        text-transform: uppercase;
        &>p{
          cursor:pointer;
          position: absolute;
          left: 50%;
          top: 50%;
          transform: translate(-50%, -50%);
          width: 60%;
          transition: color $transition_time $transition_anim_type;
        }
        & .squareHover{
          opacity: 0;
          transition: opacity $transition_time $transition_anim_type;
        }
        &:hover{
          &>p{
             background: -webkit-linear-gradient(90deg, #1293B2 10.29%, #03EEDA 26.32%, #00FFE0 86.19%, #1198B4 100%),linear-gradient(0deg, #FFFFFF, #FFFFFF);
            background-clip: text;
            -webkit-text-fill-color: transparent;
          }
          & .squareHover{
            opacity: 1;
          }
        }
      }
      &_btn{
        padding: 15px 130px;
        opacity: 0;
        // width: 450/1920*100vw;
        margin: 0 auto;
        color:$textColor1;
        display: none;
      }
      & .s1{
        bottom: 0;
        left: 150/1920*100%;
        transform: translateY(50%);
      }
      & .s2{
        top: 0;
        left: 50%;
        transform: translate(-50%, -50%);
      }
      & .s3{
        bottom: 0;
        right: 150/1920*100%;
        transform: translateY(50%);
        }
    }
  }
}
//  @import url('~/assets/scss/pages/mainPage/_block1.scss');
  // @import url('~/assets/scss/pages/mainPage/_main.scss');
</style>
