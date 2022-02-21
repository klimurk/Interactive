<template>
  <div>
    <div class="about">
      <div class="b1">
        <div class="section section--center">
          <p class="bBigTitle section__bBigTitle " :class="{'section__bBigTitle--fs18m':mobile}">
            {{ datablock1.block1.title }}
          </p>
          <p class="bSubTitle section__bSubTitle ">
            {{ datablock1.block1.text }}
          </p>
        </div>
        <div class="section" :class="{'section--right':!mobile, 'section--center':mobile, 'section--marginB':mobile}">
          <p class="bBigTitle section__bBigTitle " :class="{'section__bBigTitle--fs18m':mobile}">
            {{ datablock1.block2.title }}
          </p>
          <p class="bSubTitle section__bSubTitle ">
            {{ datablock1.block2.text }}
          </p>
        </div>
        <div class="section" :class="{'section--left':!mobile, 'section--center':mobile, 'section--marginB':mobile}">
          <p class="bSubTitle section__bSubTitle ">
            {{ datablock1.block3.subtitle }}
          </p>
          <p class="bBigTitle section__bBigTitle " :class="{'section__bBigTitle--fs18m':mobile}">
            {{ datablock1.block3.title }}
          </p>
          <p class="bSubTitle section__bSubTitle ">
            {{ datablock1.block3.text1 }}
          </p>
          <p class="bSubTitle section__bSubTitle ">
            {{ datablock1.block3.text2 }}
          </p>
        </div>
        <div class="b1__cubes">
          <v-img
            v-if="!mobile"
            :lazy-src="require('~/assets/images/sheets/AboutUs/block1/cubes.svg')"
            :src="require('~/assets/images/sheets/AboutUs/block1/cubes.svg')"
            alt=""
            max-height="100%"
            max-width="100%"
            contain
            position="left center"
          />
          <v-img
            v-if="mobile"
            :lazy-src="require('~/assets/images/sheets/AboutUs/block1/cubes_mob.svg')"
            :src="require('~/assets/images/sheets/AboutUs/block1/cubes_mob.svg')"
            alt=""
            max-height="100%"
            max-width="100%"
            contain
            position="left center"
          />
        </div>
        <div id="svg_blocks" class="percent b1__percent">
          <div v-for="percent in datablock1.svg_blocks" :key="percent.target" class="percent__col">
            <div class="bTitle percent__bTitle percent__bTitle--textFeatures">
              {{ percent.count }} %
            </div>
            <svg :id="percent.target" class="percent__svg" viewBox="0 0 86 447">
              <mask
                id="mask0_550_3"
                style="mask-type:alpha"
                maskUnits="userSpaceOnUse"
                x="0"
                y="0"
                width="86"
                height="447"
              >
                <rect width="86" height="447" fill="#C4C4C4" />
              </mask>
              <g mask="url(#mask0_550_3)">
                <mask
                  id="mask1_550_3"
                  style="mask-type:alpha"
                  maskUnits="userSpaceOnUse"
                  x="0"
                  y="0"
                  width="86"
                  height="447"
                >
                  <rect width="86" height="447" fill="white" />
                </mask>
                <g mask="url(#mask1_550_3)">
                  <path d="M0.464161 13.2691L0.781356 412.918L20.6582 446.229L20.6653 46.251L0.464161 13.2691Z" fill="url(#paint0_linear_550_3)" />
                  <path d="M0.464161 13.2691L0.781356 412.918L20.6582 446.229L20.6653 46.251L0.464161 13.2691Z" fill="black" />
                  <path d="M0.464161 13.2691L0.781356 412.918L20.6582 446.229L20.6653 46.251L0.464161 13.2691Z" fill="url(#paint1_linear_550_3)" />
                  <path d="M0.464161 13.2691L0.781356 412.918L20.6582 446.229L20.6653 46.251L0.464161 13.2691Z" fill="url(#paint2_linear_550_3)" />
                  <path d="M22.7758 446.967L83.9656 435.897L85.0027 35.1866L22.7758 46.9307L22.7758 446.967Z" fill="url(#paint3_linear_550_3)" />
                  <path d="M22.7758 446.967L83.9656 435.897L85.0027 35.1866L22.7758 46.9307L22.7758 446.967Z" fill="url(#paint4_linear_550_3)" />
                  <path d="M0.549012 13.2504L2.55078 11.751L22.7083 43.9535L20.5497 46.2508L0.549012 13.2504Z" fill="url(#paint5_linear_550_3)" />
                  <path d="M65.2162 1.48462L86.3716 34.3338L84.8798 33.1382L63.6119 0.377822L65.2162 1.48462Z" fill="url(#paint6_linear_550_3)" />
                  <path d="M2.54936 11.7553L63.7285 0.94907L84.9963 33.7094L22.8263 44.7868L2.54936 11.7553Z" fill="url(#paint7_linear_550_3)" />
                  <path d="M2.54936 11.7553L63.7285 0.94907L84.9963 33.7094L22.8263 44.7868L2.54936 11.7553Z" fill="url(#paint8_linear_550_3)" />
                  <path d="M85.0842 33.8126L85.167 35.3908L22.5536 47.2493L22.5018 44.0839L84.4996 33.3461C84.7949 33.295 85.0685 33.5133 85.0842 33.8126Z" fill="url(#paint9_linear_550_3)" />
                  <path d="M85.0842 33.8126L85.167 35.3908L22.5536 47.2493L22.5018 44.0839L84.4996 33.3461C84.7949 33.295 85.0685 33.5133 85.0842 33.8126Z" fill="black" />
                  <path d="M85.0842 33.8126L85.167 35.3908L22.5536 47.2493L22.5018 44.0839L84.4996 33.3461C84.7949 33.295 85.0685 33.5133 85.0842 33.8126Z" fill="url(#paint10_linear_550_3)" />
                  <path d="M85.0842 33.8126L85.167 35.3908L22.5536 47.2493L22.5018 44.0839L84.4996 33.3461C84.7949 33.295 85.0685 33.5133 85.0842 33.8126Z" fill="url(#paint11_linear_550_3)" />
                  <path d="M84.9531 33.529L85.0547 36.251L86.0547 34.2503L84.9531 33.529Z" fill="#C4C4C4" />
                  <path d="M84.9531 33.529L85.0547 36.251L86.0547 34.2503L84.9531 33.529Z" fill="url(#paint12_linear_550_3)" />
                  <path d="M85.0022 35.198L86.0547 34.251L85.0022 434.57L83.9688 435.897L85.0022 35.198Z" fill="url(#paint13_linear_550_3)" />
                  <path d="M20.6639 446.232L22.7808 446.97L22.8933 46.9007L20.6639 46.251L20.6639 446.232Z" fill="url(#paint14_linear_550_3)" />
                </g>
              </g>
              <defs>
                <linearGradient
                  id="paint0_linear_550_3"
                  x1="-10.7126"
                  y1="445.557"
                  x2="32.7373"
                  y2="434.679"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop offset="0.137331" stop-color="#161920" stop-opacity="0" />
                  <stop offset="0.375" stop-color="#1E232E" stop-opacity="0.58" />
                  <stop offset="0.546875" stop-color="#22356F" stop-opacity="0.6" />
                  <stop offset="0.765625" stop-color="#1097BB" stop-opacity="0.68" />
                  <stop offset="1" stop-color="#00FFE0" />
                </linearGradient>
                <linearGradient
                  id="paint1_linear_550_3"
                  x1="7.55643"
                  y1="445.365"
                  x2="40.9775"
                  y2="433.409"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint2_linear_550_3"
                  x1="-31.8602"
                  y1="287.474"
                  x2="5.8803"
                  y2="282.554"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint3_linear_550_3"
                  x1="22.7721"
                  y1="446.393"
                  x2="85.0504"
                  y2="379.941"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint4_linear_550_3"
                  x1="-89.9492"
                  y1="263.251"
                  x2="105.226"
                  y2="295.818"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint5_linear_550_3"
                  x1="7.51047"
                  y1="19.6018"
                  x2="4.98654"
                  y2="21.1815"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.598958" stop-color="#1097BB" />
                  <stop offset="0.695377" stop-color="#0BD3CC" />
                </linearGradient>
                <linearGradient
                  id="paint6_linear_550_3"
                  x1="58.9141"
                  y1="51.2091"
                  x2="90.2322"
                  y2="41.0451"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.48179" stop-color="#162650" />
                  <stop offset="0.687542" stop-color="#29649B" />
                  <stop offset="0.864308" stop-color="#00BECB" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint7_linear_550_3"
                  x1="5.63666"
                  y1="38.5404"
                  x2="70.3968"
                  y2="-5.05827"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint8_linear_550_3"
                  x1="-24.0299"
                  y1="-15.2316"
                  x2="76.5073"
                  y2="17.1338"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint9_linear_550_3"
                  x1="-22.8361"
                  y1="57.484"
                  x2="-13.1437"
                  y2="11.2689"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop offset="0.137331" stop-color="#161920" stop-opacity="0" />
                  <stop offset="0.375" stop-color="#1E232E" stop-opacity="0.58" />
                  <stop offset="0.546875" stop-color="#22356F" stop-opacity="0.6" />
                  <stop offset="0.765625" stop-color="#1097BB" stop-opacity="0.68" />
                  <stop offset="1" stop-color="#00FFE0" />
                </linearGradient>
                <linearGradient
                  id="paint10_linear_550_3"
                  x1="4.95096"
                  y1="52.0663"
                  x2="6.26729"
                  y2="30.1824"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint11_linear_550_3"
                  x1="5.1438"
                  y1="44.0955"
                  x2="14.8663"
                  y2="64.9701"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint12_linear_550_3"
                  x1="84.5209"
                  y1="34.6609"
                  x2="86.7023"
                  y2="34.0304"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#1097BB" stop-opacity="0.68" />
                  <stop offset="0.0001" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#00FFE0" />
                </linearGradient>
                <linearGradient
                  id="paint13_linear_550_3"
                  x1="84.4876"
                  y1="435.79"
                  x2="86.2378"
                  y2="379.253"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop offset="0.23252" stop-color="#066979" />
                  <stop offset="1" stop-color="#00FADE" />
                </linearGradient>
                <linearGradient
                  id="paint14_linear_550_3"
                  x1="20.5861"
                  y1="419.87"
                  x2="23.6864"
                  y2="419.889"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#1385AC" />
                  <stop offset="0.559233" stop-color="#21366F" />
                  <stop offset="1" stop-color="#1D3165" />
                </linearGradient>
              </defs>
            </svg>
          </div>
          <!-- <div class="percent__col">
            <div class="percent__num">
              {{ datablock1.svg_blocks[1].count }} %
            </div>
            <svg id="svgBlock2" class="svg_block" viewBox="0 0 86 447">
              <mask
                id="mask0_550_3"
                style="mask-type:alpha"
                maskUnits="userSpaceOnUse"
                x="0"
                y="0"
                width="86"
                height="447"
              >
                <rect width="86" height="447" fill="#C4C4C4" />
              </mask>
              <g mask="url(#mask0_550_3)">
                <mask
                  id="mask1_550_3"
                  style="mask-type:alpha"
                  maskUnits="userSpaceOnUse"
                  x="0"
                  y="0"
                  width="86"
                  height="447"
                >
                  <rect width="86" height="447" fill="white" />
                </mask>
                <g mask="url(#mask1_550_3)">
                  <path d="M0.464161 13.2691L0.781356 412.918L20.6582 446.229L20.6653 46.251L0.464161 13.2691Z" fill="url(#paint0_linear_550_3)" />
                  <path d="M0.464161 13.2691L0.781356 412.918L20.6582 446.229L20.6653 46.251L0.464161 13.2691Z" fill="black" />
                  <path d="M0.464161 13.2691L0.781356 412.918L20.6582 446.229L20.6653 46.251L0.464161 13.2691Z" fill="url(#paint1_linear_550_3)" />
                  <path d="M0.464161 13.2691L0.781356 412.918L20.6582 446.229L20.6653 46.251L0.464161 13.2691Z" fill="url(#paint2_linear_550_3)" />
                  <path d="M22.7758 446.967L83.9656 435.897L85.0027 35.1866L22.7758 46.9307L22.7758 446.967Z" fill="url(#paint3_linear_550_3)" />
                  <path d="M22.7758 446.967L83.9656 435.897L85.0027 35.1866L22.7758 46.9307L22.7758 446.967Z" fill="url(#paint4_linear_550_3)" />
                  <path d="M0.549012 13.2504L2.55078 11.751L22.7083 43.9535L20.5497 46.2508L0.549012 13.2504Z" fill="url(#paint5_linear_550_3)" />
                  <path d="M65.2162 1.48462L86.3716 34.3338L84.8798 33.1382L63.6119 0.377822L65.2162 1.48462Z" fill="url(#paint6_linear_550_3)" />
                  <path d="M2.54936 11.7553L63.7285 0.94907L84.9963 33.7094L22.8263 44.7868L2.54936 11.7553Z" fill="url(#paint7_linear_550_3)" />
                  <path d="M2.54936 11.7553L63.7285 0.94907L84.9963 33.7094L22.8263 44.7868L2.54936 11.7553Z" fill="url(#paint8_linear_550_3)" />
                  <path d="M85.0842 33.8126L85.167 35.3908L22.5536 47.2493L22.5018 44.0839L84.4996 33.3461C84.7949 33.295 85.0685 33.5133 85.0842 33.8126Z" fill="url(#paint9_linear_550_3)" />
                  <path d="M85.0842 33.8126L85.167 35.3908L22.5536 47.2493L22.5018 44.0839L84.4996 33.3461C84.7949 33.295 85.0685 33.5133 85.0842 33.8126Z" fill="black" />
                  <path d="M85.0842 33.8126L85.167 35.3908L22.5536 47.2493L22.5018 44.0839L84.4996 33.3461C84.7949 33.295 85.0685 33.5133 85.0842 33.8126Z" fill="url(#paint10_linear_550_3)" />
                  <path d="M85.0842 33.8126L85.167 35.3908L22.5536 47.2493L22.5018 44.0839L84.4996 33.3461C84.7949 33.295 85.0685 33.5133 85.0842 33.8126Z" fill="url(#paint11_linear_550_3)" />
                  <path d="M84.9531 33.529L85.0547 36.251L86.0547 34.2503L84.9531 33.529Z" fill="#C4C4C4" />
                  <path d="M84.9531 33.529L85.0547 36.251L86.0547 34.2503L84.9531 33.529Z" fill="url(#paint12_linear_550_3)" />
                  <path d="M85.0022 35.198L86.0547 34.251L85.0022 434.57L83.9688 435.897L85.0022 35.198Z" fill="url(#paint13_linear_550_3)" />
                  <path d="M20.6639 446.232L22.7808 446.97L22.8933 46.9007L20.6639 46.251L20.6639 446.232Z" fill="url(#paint14_linear_550_3)" />
                </g>
              </g>
              <defs>
                <linearGradient
                  id="paint0_linear_550_3"
                  x1="-10.7126"
                  y1="445.557"
                  x2="32.7373"
                  y2="434.679"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop offset="0.137331" stop-color="#161920" stop-opacity="0" />
                  <stop offset="0.375" stop-color="#1E232E" stop-opacity="0.58" />
                  <stop offset="0.546875" stop-color="#22356F" stop-opacity="0.6" />
                  <stop offset="0.765625" stop-color="#1097BB" stop-opacity="0.68" />
                  <stop offset="1" stop-color="#00FFE0" />
                </linearGradient>
                <linearGradient
                  id="paint1_linear_550_3"
                  x1="7.55643"
                  y1="445.365"
                  x2="40.9775"
                  y2="433.409"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint2_linear_550_3"
                  x1="-31.8602"
                  y1="287.474"
                  x2="5.8803"
                  y2="282.554"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint3_linear_550_3"
                  x1="22.7721"
                  y1="446.393"
                  x2="85.0504"
                  y2="379.941"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint4_linear_550_3"
                  x1="-89.9492"
                  y1="263.251"
                  x2="105.226"
                  y2="295.818"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint5_linear_550_3"
                  x1="7.51047"
                  y1="19.6018"
                  x2="4.98654"
                  y2="21.1815"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.598958" stop-color="#1097BB" />
                  <stop offset="0.695377" stop-color="#0BD3CC" />
                </linearGradient>
                <linearGradient
                  id="paint6_linear_550_3"
                  x1="58.9141"
                  y1="51.2091"
                  x2="90.2322"
                  y2="41.0451"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.48179" stop-color="#162650" />
                  <stop offset="0.687542" stop-color="#29649B" />
                  <stop offset="0.864308" stop-color="#00BECB" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint7_linear_550_3"
                  x1="5.63666"
                  y1="38.5404"
                  x2="70.3968"
                  y2="-5.05827"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint8_linear_550_3"
                  x1="-24.0299"
                  y1="-15.2316"
                  x2="76.5073"
                  y2="17.1338"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint9_linear_550_3"
                  x1="-22.8361"
                  y1="57.484"
                  x2="-13.1437"
                  y2="11.2689"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop offset="0.137331" stop-color="#161920" stop-opacity="0" />
                  <stop offset="0.375" stop-color="#1E232E" stop-opacity="0.58" />
                  <stop offset="0.546875" stop-color="#22356F" stop-opacity="0.6" />
                  <stop offset="0.765625" stop-color="#1097BB" stop-opacity="0.68" />
                  <stop offset="1" stop-color="#00FFE0" />
                </linearGradient>
                <linearGradient
                  id="paint10_linear_550_3"
                  x1="4.95096"
                  y1="52.0663"
                  x2="6.26729"
                  y2="30.1824"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint11_linear_550_3"
                  x1="5.1438"
                  y1="44.0955"
                  x2="14.8663"
                  y2="64.9701"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint12_linear_550_3"
                  x1="84.5209"
                  y1="34.6609"
                  x2="86.7023"
                  y2="34.0304"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#1097BB" stop-opacity="0.68" />
                  <stop offset="0.0001" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#00FFE0" />
                </linearGradient>
                <linearGradient
                  id="paint13_linear_550_3"
                  x1="84.4876"
                  y1="435.79"
                  x2="86.2378"
                  y2="379.253"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop offset="0.23252" stop-color="#066979" />
                  <stop offset="1" stop-color="#00FADE" />
                </linearGradient>
                <linearGradient
                  id="paint14_linear_550_3"
                  x1="20.5861"
                  y1="419.87"
                  x2="23.6864"
                  y2="419.889"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#1385AC" />
                  <stop offset="0.559233" stop-color="#21366F" />
                  <stop offset="1" stop-color="#1D3165" />
                </linearGradient>
              </defs>
            </svg>
          </div>
          <div class="percent__col">
            <div class="percent__num">
              {{ datablock1.svg_blocks[2].count }} %
            </div>
            <svg id="svgBlock3" class="svg_block" viewBox="0 0 86 447">
              <mask
                id="mask0_550_3"
                style="mask-type:alpha"
                maskUnits="userSpaceOnUse"
                x="0"
                y="0"
                width="86"
                height="447"
              >
                <rect width="86" height="447" fill="#C4C4C4" />
              </mask>
              <g mask="url(#mask0_550_3)">
                <mask
                  id="mask1_550_3"
                  style="mask-type:alpha"
                  maskUnits="userSpaceOnUse"
                  x="0"
                  y="0"
                  width="86"
                  height="447"
                >
                  <rect width="86" height="447" fill="white" />
                </mask>
                <g mask="url(#mask1_550_3)">
                  <path d="M0.464161 13.2691L0.781356 412.918L20.6582 446.229L20.6653 46.251L0.464161 13.2691Z" fill="url(#paint0_linear_550_3)" />
                  <path d="M0.464161 13.2691L0.781356 412.918L20.6582 446.229L20.6653 46.251L0.464161 13.2691Z" fill="black" />
                  <path d="M0.464161 13.2691L0.781356 412.918L20.6582 446.229L20.6653 46.251L0.464161 13.2691Z" fill="url(#paint1_linear_550_3)" />
                  <path d="M0.464161 13.2691L0.781356 412.918L20.6582 446.229L20.6653 46.251L0.464161 13.2691Z" fill="url(#paint2_linear_550_3)" />
                  <path d="M22.7758 446.967L83.9656 435.897L85.0027 35.1866L22.7758 46.9307L22.7758 446.967Z" fill="url(#paint3_linear_550_3)" />
                  <path d="M22.7758 446.967L83.9656 435.897L85.0027 35.1866L22.7758 46.9307L22.7758 446.967Z" fill="url(#paint4_linear_550_3)" />
                  <path d="M0.549012 13.2504L2.55078 11.751L22.7083 43.9535L20.5497 46.2508L0.549012 13.2504Z" fill="url(#paint5_linear_550_3)" />
                  <path d="M65.2162 1.48462L86.3716 34.3338L84.8798 33.1382L63.6119 0.377822L65.2162 1.48462Z" fill="url(#paint6_linear_550_3)" />
                  <path d="M2.54936 11.7553L63.7285 0.94907L84.9963 33.7094L22.8263 44.7868L2.54936 11.7553Z" fill="url(#paint7_linear_550_3)" />
                  <path d="M2.54936 11.7553L63.7285 0.94907L84.9963 33.7094L22.8263 44.7868L2.54936 11.7553Z" fill="url(#paint8_linear_550_3)" />
                  <path d="M85.0842 33.8126L85.167 35.3908L22.5536 47.2493L22.5018 44.0839L84.4996 33.3461C84.7949 33.295 85.0685 33.5133 85.0842 33.8126Z" fill="url(#paint9_linear_550_3)" />
                  <path d="M85.0842 33.8126L85.167 35.3908L22.5536 47.2493L22.5018 44.0839L84.4996 33.3461C84.7949 33.295 85.0685 33.5133 85.0842 33.8126Z" fill="black" />
                  <path d="M85.0842 33.8126L85.167 35.3908L22.5536 47.2493L22.5018 44.0839L84.4996 33.3461C84.7949 33.295 85.0685 33.5133 85.0842 33.8126Z" fill="url(#paint10_linear_550_3)" />
                  <path d="M85.0842 33.8126L85.167 35.3908L22.5536 47.2493L22.5018 44.0839L84.4996 33.3461C84.7949 33.295 85.0685 33.5133 85.0842 33.8126Z" fill="url(#paint11_linear_550_3)" />
                  <path d="M84.9531 33.529L85.0547 36.251L86.0547 34.2503L84.9531 33.529Z" fill="#C4C4C4" />
                  <path d="M84.9531 33.529L85.0547 36.251L86.0547 34.2503L84.9531 33.529Z" fill="url(#paint12_linear_550_3)" />
                  <path d="M85.0022 35.198L86.0547 34.251L85.0022 434.57L83.9688 435.897L85.0022 35.198Z" fill="url(#paint13_linear_550_3)" />
                  <path d="M20.6639 446.232L22.7808 446.97L22.8933 46.9007L20.6639 46.251L20.6639 446.232Z" fill="url(#paint14_linear_550_3)" />
                </g>
              </g>
              <defs>
                <linearGradient
                  id="paint0_linear_550_3"
                  x1="-10.7126"
                  y1="445.557"
                  x2="32.7373"
                  y2="434.679"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop offset="0.137331" stop-color="#161920" stop-opacity="0" />
                  <stop offset="0.375" stop-color="#1E232E" stop-opacity="0.58" />
                  <stop offset="0.546875" stop-color="#22356F" stop-opacity="0.6" />
                  <stop offset="0.765625" stop-color="#1097BB" stop-opacity="0.68" />
                  <stop offset="1" stop-color="#00FFE0" />
                </linearGradient>
                <linearGradient
                  id="paint1_linear_550_3"
                  x1="7.55643"
                  y1="445.365"
                  x2="40.9775"
                  y2="433.409"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint2_linear_550_3"
                  x1="-31.8602"
                  y1="287.474"
                  x2="5.8803"
                  y2="282.554"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint3_linear_550_3"
                  x1="22.7721"
                  y1="446.393"
                  x2="85.0504"
                  y2="379.941"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint4_linear_550_3"
                  x1="-89.9492"
                  y1="263.251"
                  x2="105.226"
                  y2="295.818"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint5_linear_550_3"
                  x1="7.51047"
                  y1="19.6018"
                  x2="4.98654"
                  y2="21.1815"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.598958" stop-color="#1097BB" />
                  <stop offset="0.695377" stop-color="#0BD3CC" />
                </linearGradient>
                <linearGradient
                  id="paint6_linear_550_3"
                  x1="58.9141"
                  y1="51.2091"
                  x2="90.2322"
                  y2="41.0451"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.48179" stop-color="#162650" />
                  <stop offset="0.687542" stop-color="#29649B" />
                  <stop offset="0.864308" stop-color="#00BECB" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint7_linear_550_3"
                  x1="5.63666"
                  y1="38.5404"
                  x2="70.3968"
                  y2="-5.05827"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint8_linear_550_3"
                  x1="-24.0299"
                  y1="-15.2316"
                  x2="76.5073"
                  y2="17.1338"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint9_linear_550_3"
                  x1="-22.8361"
                  y1="57.484"
                  x2="-13.1437"
                  y2="11.2689"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop offset="0.137331" stop-color="#161920" stop-opacity="0" />
                  <stop offset="0.375" stop-color="#1E232E" stop-opacity="0.58" />
                  <stop offset="0.546875" stop-color="#22356F" stop-opacity="0.6" />
                  <stop offset="0.765625" stop-color="#1097BB" stop-opacity="0.68" />
                  <stop offset="1" stop-color="#00FFE0" />
                </linearGradient>
                <linearGradient
                  id="paint10_linear_550_3"
                  x1="4.95096"
                  y1="52.0663"
                  x2="6.26729"
                  y2="30.1824"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint11_linear_550_3"
                  x1="5.1438"
                  y1="44.0955"
                  x2="14.8663"
                  y2="64.9701"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint12_linear_550_3"
                  x1="84.5209"
                  y1="34.6609"
                  x2="86.7023"
                  y2="34.0304"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#1097BB" stop-opacity="0.68" />
                  <stop offset="0.0001" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#00FFE0" />
                </linearGradient>
                <linearGradient
                  id="paint13_linear_550_3"
                  x1="84.4876"
                  y1="435.79"
                  x2="86.2378"
                  y2="379.253"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop offset="0.23252" stop-color="#066979" />
                  <stop offset="1" stop-color="#00FADE" />
                </linearGradient>
                <linearGradient
                  id="paint14_linear_550_3"
                  x1="20.5861"
                  y1="419.87"
                  x2="23.6864"
                  y2="419.889"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#1385AC" />
                  <stop offset="0.559233" stop-color="#21366F" />
                  <stop offset="1" stop-color="#1D3165" />
                </linearGradient>
              </defs>
            </svg>
          </div>
          <div class="percent__col">
            <div class="percent__num">
              {{ datablock1.svg_blocks[3].count }} %
            </div>
            <svg id="svgBlock4" class="svg_block" viewBox="0 0 86 447">
              <mask
                id="mask0_550_3"
                style="mask-type:alpha"
                maskUnits="userSpaceOnUse"
                x="0"
                y="0"
                width="86"
                height="447"
              >
                <rect width="86" height="447" fill="#C4C4C4" />
              </mask>
              <g mask="url(#mask0_550_3)">
                <mask
                  id="mask1_550_3"
                  style="mask-type:alpha"
                  maskUnits="userSpaceOnUse"
                  x="0"
                  y="0"
                  width="86"
                  height="447"
                >
                  <rect width="86" height="447" fill="white" />
                </mask>
                <g mask="url(#mask1_550_3)">
                  <path d="M0.464161 13.2691L0.781356 412.918L20.6582 446.229L20.6653 46.251L0.464161 13.2691Z" fill="url(#paint0_linear_550_3)" />
                  <path d="M0.464161 13.2691L0.781356 412.918L20.6582 446.229L20.6653 46.251L0.464161 13.2691Z" fill="black" />
                  <path d="M0.464161 13.2691L0.781356 412.918L20.6582 446.229L20.6653 46.251L0.464161 13.2691Z" fill="url(#paint1_linear_550_3)" />
                  <path d="M0.464161 13.2691L0.781356 412.918L20.6582 446.229L20.6653 46.251L0.464161 13.2691Z" fill="url(#paint2_linear_550_3)" />
                  <path d="M22.7758 446.967L83.9656 435.897L85.0027 35.1866L22.7758 46.9307L22.7758 446.967Z" fill="url(#paint3_linear_550_3)" />
                  <path d="M22.7758 446.967L83.9656 435.897L85.0027 35.1866L22.7758 46.9307L22.7758 446.967Z" fill="url(#paint4_linear_550_3)" />
                  <path d="M0.549012 13.2504L2.55078 11.751L22.7083 43.9535L20.5497 46.2508L0.549012 13.2504Z" fill="url(#paint5_linear_550_3)" />
                  <path d="M65.2162 1.48462L86.3716 34.3338L84.8798 33.1382L63.6119 0.377822L65.2162 1.48462Z" fill="url(#paint6_linear_550_3)" />
                  <path d="M2.54936 11.7553L63.7285 0.94907L84.9963 33.7094L22.8263 44.7868L2.54936 11.7553Z" fill="url(#paint7_linear_550_3)" />
                  <path d="M2.54936 11.7553L63.7285 0.94907L84.9963 33.7094L22.8263 44.7868L2.54936 11.7553Z" fill="url(#paint8_linear_550_3)" />
                  <path d="M85.0842 33.8126L85.167 35.3908L22.5536 47.2493L22.5018 44.0839L84.4996 33.3461C84.7949 33.295 85.0685 33.5133 85.0842 33.8126Z" fill="url(#paint9_linear_550_3)" />
                  <path d="M85.0842 33.8126L85.167 35.3908L22.5536 47.2493L22.5018 44.0839L84.4996 33.3461C84.7949 33.295 85.0685 33.5133 85.0842 33.8126Z" fill="black" />
                  <path d="M85.0842 33.8126L85.167 35.3908L22.5536 47.2493L22.5018 44.0839L84.4996 33.3461C84.7949 33.295 85.0685 33.5133 85.0842 33.8126Z" fill="url(#paint10_linear_550_3)" />
                  <path d="M85.0842 33.8126L85.167 35.3908L22.5536 47.2493L22.5018 44.0839L84.4996 33.3461C84.7949 33.295 85.0685 33.5133 85.0842 33.8126Z" fill="url(#paint11_linear_550_3)" />
                  <path d="M84.9531 33.529L85.0547 36.251L86.0547 34.2503L84.9531 33.529Z" fill="#C4C4C4" />
                  <path d="M84.9531 33.529L85.0547 36.251L86.0547 34.2503L84.9531 33.529Z" fill="url(#paint12_linear_550_3)" />
                  <path d="M85.0022 35.198L86.0547 34.251L85.0022 434.57L83.9688 435.897L85.0022 35.198Z" fill="url(#paint13_linear_550_3)" />
                  <path d="M20.6639 446.232L22.7808 446.97L22.8933 46.9007L20.6639 46.251L20.6639 446.232Z" fill="url(#paint14_linear_550_3)" />
                </g>
              </g>
              <defs>
                <linearGradient
                  id="paint0_linear_550_3"
                  x1="-10.7126"
                  y1="445.557"
                  x2="32.7373"
                  y2="434.679"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop offset="0.137331" stop-color="#161920" stop-opacity="0" />
                  <stop offset="0.375" stop-color="#1E232E" stop-opacity="0.58" />
                  <stop offset="0.546875" stop-color="#22356F" stop-opacity="0.6" />
                  <stop offset="0.765625" stop-color="#1097BB" stop-opacity="0.68" />
                  <stop offset="1" stop-color="#00FFE0" />
                </linearGradient>
                <linearGradient
                  id="paint1_linear_550_3"
                  x1="7.55643"
                  y1="445.365"
                  x2="40.9775"
                  y2="433.409"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint2_linear_550_3"
                  x1="-31.8602"
                  y1="287.474"
                  x2="5.8803"
                  y2="282.554"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint3_linear_550_3"
                  x1="22.7721"
                  y1="446.393"
                  x2="85.0504"
                  y2="379.941"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint4_linear_550_3"
                  x1="-89.9492"
                  y1="263.251"
                  x2="105.226"
                  y2="295.818"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint5_linear_550_3"
                  x1="7.51047"
                  y1="19.6018"
                  x2="4.98654"
                  y2="21.1815"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.598958" stop-color="#1097BB" />
                  <stop offset="0.695377" stop-color="#0BD3CC" />
                </linearGradient>
                <linearGradient
                  id="paint6_linear_550_3"
                  x1="58.9141"
                  y1="51.2091"
                  x2="90.2322"
                  y2="41.0451"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.48179" stop-color="#162650" />
                  <stop offset="0.687542" stop-color="#29649B" />
                  <stop offset="0.864308" stop-color="#00BECB" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint7_linear_550_3"
                  x1="5.63666"
                  y1="38.5404"
                  x2="70.3968"
                  y2="-5.05827"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint8_linear_550_3"
                  x1="-24.0299"
                  y1="-15.2316"
                  x2="76.5073"
                  y2="17.1338"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint9_linear_550_3"
                  x1="-22.8361"
                  y1="57.484"
                  x2="-13.1437"
                  y2="11.2689"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop offset="0.137331" stop-color="#161920" stop-opacity="0" />
                  <stop offset="0.375" stop-color="#1E232E" stop-opacity="0.58" />
                  <stop offset="0.546875" stop-color="#22356F" stop-opacity="0.6" />
                  <stop offset="0.765625" stop-color="#1097BB" stop-opacity="0.68" />
                  <stop offset="1" stop-color="#00FFE0" />
                </linearGradient>
                <linearGradient
                  id="paint10_linear_550_3"
                  x1="4.95096"
                  y1="52.0663"
                  x2="6.26729"
                  y2="30.1824"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint11_linear_550_3"
                  x1="5.1438"
                  y1="44.0955"
                  x2="14.8663"
                  y2="64.9701"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint12_linear_550_3"
                  x1="84.5209"
                  y1="34.6609"
                  x2="86.7023"
                  y2="34.0304"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#1097BB" stop-opacity="0.68" />
                  <stop offset="0.0001" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#00FFE0" />
                </linearGradient>
                <linearGradient
                  id="paint13_linear_550_3"
                  x1="84.4876"
                  y1="435.79"
                  x2="86.2378"
                  y2="379.253"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop offset="0.23252" stop-color="#066979" />
                  <stop offset="1" stop-color="#00FADE" />
                </linearGradient>
                <linearGradient
                  id="paint14_linear_550_3"
                  x1="20.5861"
                  y1="419.87"
                  x2="23.6864"
                  y2="419.889"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#1385AC" />
                  <stop offset="0.559233" stop-color="#21366F" />
                  <stop offset="1" stop-color="#1D3165" />
                </linearGradient>
              </defs>
            </svg>
          </div>
          <div class="percent__col">
            <div class="percent__num">
              {{ datablock1.svg_blocks[4].count }} %
            </div>
            <svg id="svgBlock5" class="svg_block" viewBox="0 0 86 447">
              <mask
                id="mask0_550_3"
                style="mask-type:alpha"
                maskUnits="userSpaceOnUse"
                x="0"
                y="0"
                width="86"
                height="447"
              >
                <rect width="86" height="447" fill="#C4C4C4" />
              </mask>
              <g mask="url(#mask0_550_3)">
                <mask
                  id="mask1_550_3"
                  style="mask-type:alpha"
                  maskUnits="userSpaceOnUse"
                  x="0"
                  y="0"
                  width="86"
                  height="447"
                >
                  <rect width="86" height="447" fill="white" />
                </mask>
                <g mask="url(#mask1_550_3)">
                  <path d="M0.464161 13.2691L0.781356 412.918L20.6582 446.229L20.6653 46.251L0.464161 13.2691Z" fill="url(#paint0_linear_550_3)" />
                  <path d="M0.464161 13.2691L0.781356 412.918L20.6582 446.229L20.6653 46.251L0.464161 13.2691Z" fill="black" />
                  <path d="M0.464161 13.2691L0.781356 412.918L20.6582 446.229L20.6653 46.251L0.464161 13.2691Z" fill="url(#paint1_linear_550_3)" />
                  <path d="M0.464161 13.2691L0.781356 412.918L20.6582 446.229L20.6653 46.251L0.464161 13.2691Z" fill="url(#paint2_linear_550_3)" />
                  <path d="M22.7758 446.967L83.9656 435.897L85.0027 35.1866L22.7758 46.9307L22.7758 446.967Z" fill="url(#paint3_linear_550_3)" />
                  <path d="M22.7758 446.967L83.9656 435.897L85.0027 35.1866L22.7758 46.9307L22.7758 446.967Z" fill="url(#paint4_linear_550_3)" />
                  <path d="M0.549012 13.2504L2.55078 11.751L22.7083 43.9535L20.5497 46.2508L0.549012 13.2504Z" fill="url(#paint5_linear_550_3)" />
                  <path d="M65.2162 1.48462L86.3716 34.3338L84.8798 33.1382L63.6119 0.377822L65.2162 1.48462Z" fill="url(#paint6_linear_550_3)" />
                  <path d="M2.54936 11.7553L63.7285 0.94907L84.9963 33.7094L22.8263 44.7868L2.54936 11.7553Z" fill="url(#paint7_linear_550_3)" />
                  <path d="M2.54936 11.7553L63.7285 0.94907L84.9963 33.7094L22.8263 44.7868L2.54936 11.7553Z" fill="url(#paint8_linear_550_3)" />
                  <path d="M85.0842 33.8126L85.167 35.3908L22.5536 47.2493L22.5018 44.0839L84.4996 33.3461C84.7949 33.295 85.0685 33.5133 85.0842 33.8126Z" fill="url(#paint9_linear_550_3)" />
                  <path d="M85.0842 33.8126L85.167 35.3908L22.5536 47.2493L22.5018 44.0839L84.4996 33.3461C84.7949 33.295 85.0685 33.5133 85.0842 33.8126Z" fill="black" />
                  <path d="M85.0842 33.8126L85.167 35.3908L22.5536 47.2493L22.5018 44.0839L84.4996 33.3461C84.7949 33.295 85.0685 33.5133 85.0842 33.8126Z" fill="url(#paint10_linear_550_3)" />
                  <path d="M85.0842 33.8126L85.167 35.3908L22.5536 47.2493L22.5018 44.0839L84.4996 33.3461C84.7949 33.295 85.0685 33.5133 85.0842 33.8126Z" fill="url(#paint11_linear_550_3)" />
                  <path d="M84.9531 33.529L85.0547 36.251L86.0547 34.2503L84.9531 33.529Z" fill="#C4C4C4" />
                  <path d="M84.9531 33.529L85.0547 36.251L86.0547 34.2503L84.9531 33.529Z" fill="url(#paint12_linear_550_3)" />
                  <path d="M85.0022 35.198L86.0547 34.251L85.0022 434.57L83.9688 435.897L85.0022 35.198Z" fill="url(#paint13_linear_550_3)" />
                  <path d="M20.6639 446.232L22.7808 446.97L22.8933 46.9007L20.6639 46.251L20.6639 446.232Z" fill="url(#paint14_linear_550_3)" />
                </g>
              </g>
              <defs>
                <linearGradient
                  id="paint0_linear_550_3"
                  x1="-10.7126"
                  y1="445.557"
                  x2="32.7373"
                  y2="434.679"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop offset="0.137331" stop-color="#161920" stop-opacity="0" />
                  <stop offset="0.375" stop-color="#1E232E" stop-opacity="0.58" />
                  <stop offset="0.546875" stop-color="#22356F" stop-opacity="0.6" />
                  <stop offset="0.765625" stop-color="#1097BB" stop-opacity="0.68" />
                  <stop offset="1" stop-color="#00FFE0" />
                </linearGradient>
                <linearGradient
                  id="paint1_linear_550_3"
                  x1="7.55643"
                  y1="445.365"
                  x2="40.9775"
                  y2="433.409"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint2_linear_550_3"
                  x1="-31.8602"
                  y1="287.474"
                  x2="5.8803"
                  y2="282.554"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint3_linear_550_3"
                  x1="22.7721"
                  y1="446.393"
                  x2="85.0504"
                  y2="379.941"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint4_linear_550_3"
                  x1="-89.9492"
                  y1="263.251"
                  x2="105.226"
                  y2="295.818"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint5_linear_550_3"
                  x1="7.51047"
                  y1="19.6018"
                  x2="4.98654"
                  y2="21.1815"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#22356F" />
                  <stop offset="0.598958" stop-color="#1097BB" />
                  <stop offset="0.695377" stop-color="#0BD3CC" />
                </linearGradient>
                <linearGradient
                  id="paint6_linear_550_3"
                  x1="58.9141"
                  y1="51.2091"
                  x2="90.2322"
                  y2="41.0451"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.48179" stop-color="#162650" />
                  <stop offset="0.687542" stop-color="#29649B" />
                  <stop offset="0.864308" stop-color="#00BECB" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint7_linear_550_3"
                  x1="5.63666"
                  y1="38.5404"
                  x2="70.3968"
                  y2="-5.05827"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint8_linear_550_3"
                  x1="-24.0299"
                  y1="-15.2316"
                  x2="76.5073"
                  y2="17.1338"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint9_linear_550_3"
                  x1="-22.8361"
                  y1="57.484"
                  x2="-13.1437"
                  y2="11.2689"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop offset="0.137331" stop-color="#161920" stop-opacity="0" />
                  <stop offset="0.375" stop-color="#1E232E" stop-opacity="0.58" />
                  <stop offset="0.546875" stop-color="#22356F" stop-opacity="0.6" />
                  <stop offset="0.765625" stop-color="#1097BB" stop-opacity="0.68" />
                  <stop offset="1" stop-color="#00FFE0" />
                </linearGradient>
                <linearGradient
                  id="paint10_linear_550_3"
                  x1="4.95096"
                  y1="52.0663"
                  x2="6.26729"
                  y2="30.1824"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint11_linear_550_3"
                  x1="5.1438"
                  y1="44.0955"
                  x2="14.8663"
                  y2="64.9701"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#010611" />
                  <stop offset="0.224899" stop-color="#162650" />
                  <stop offset="0.463542" stop-color="#29649B" />
                  <stop offset="1" stop-color="#00FDDF" />
                </linearGradient>
                <linearGradient
                  id="paint12_linear_550_3"
                  x1="84.5209"
                  y1="34.6609"
                  x2="86.7023"
                  y2="34.0304"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#1097BB" stop-opacity="0.68" />
                  <stop offset="0.0001" stop-color="#1097BB" />
                  <stop offset="1" stop-color="#00FFE0" />
                </linearGradient>
                <linearGradient
                  id="paint13_linear_550_3"
                  x1="84.4876"
                  y1="435.79"
                  x2="86.2378"
                  y2="379.253"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop offset="0.23252" stop-color="#066979" />
                  <stop offset="1" stop-color="#00FADE" />
                </linearGradient>
                <linearGradient
                  id="paint14_linear_550_3"
                  x1="20.5861"
                  y1="419.87"
                  x2="23.6864"
                  y2="419.889"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#1385AC" />
                  <stop offset="0.559233" stop-color="#21366F" />
                  <stop offset="1" stop-color="#1D3165" />
                </linearGradient>
              </defs>
            </svg>
          </div> -->
        </div>
      </div>
      <div class="b2">
        <div class="b2__col">
          <p class="bBigTitle b2__bBigTitle" :class="{'b2__bBigTitle--fs18m':mobile}">
            {{ datablock2.soros }}
          </p>
        </div>
        <v-img v-if="!mobile" max-height="30vw" lazy-src="/assets/images/sheets/AboutUs/block2/soros.png" :src="require('~/assets/images/sheets/AboutUs/block2/soros.png')" />
        <div class="b2__col">
          <div class="bTitle b2__bTitle">
            {{ datablock2.text }}
            <svg class="b2__svg b2__svg--1" viewBox="0 0 48 33">
              <path d="M20.2232 32.0088L34.611 0.00878906H47.5L37.3686 32.0088H20.2232ZM0.5 32.0088L15.0676 0.00878906H27.9566L17.7054 32.0088H0.5Z" fill="#00FDDF" />
            </svg>
            <svg class="b2__svg b2__svg--2" viewBox="0 0 47 34">
              <path d="M19.5434 33.3438L29.7946 0.34375H47L32.4324 33.3438H19.5434ZM0 33.3438L10.1314 0.34375H27.2768L12.889 33.3438H0Z" fill="#00FDDF" />
            </svg>
          </div>
        </div>
        <v-img v-if="mobile" lazy-src="/assets/images/sheets/AboutUs/block2/soros.png" :src="require('~/assets/images/sheets/AboutUs/block2/soros.png')" />
      </div>
      <div class="b3">
        <div class="b3__col">
          <div class="b3__block">
            <p class="bBigTitle b3__bBigTitle ">
              {{ datablock3.block[0].title }}
            </p>
            <p class="bSubTitle b3__bSubTitle text">
              {{ datablock3.block[0].text }}
            </p>
          </div>
          <v-img lazy-src="/assets/images/sheets/AboutUs/block3/photoSmall.png" :src="require('~/assets/images/sheets/AboutUs/block3/photoSmall.png')" />
        </div>
        <div class="b3__col">
          <v-img v-if="!mobile" lazy-src="/assets/images/sheets/AboutUs/block3/photoBig.png" :src="require('~/assets/images/sheets/AboutUs/block3/photoBig.png')" />
        </div>
        <div class="b3__col">
          <div class="b3__block">
            <p class="bBigTitle b3__bBigTitle">
              {{ datablock3.block[1].title }}
            </p>
            <p class="bSubTitle b3__bSubTitle">
              {{ datablock3.block[1].text }}
            </p>
          </div>
          <v-img v-if="mobile" lazy-src="/assets/images/sheets/AboutUs/block3/photoBig.png" :src="require('~/assets/images/sheets/AboutUs/block3/photoBig.png')" />
          <div class="b3__block">
            <p class="bBigTitle b3__bBigTitle ">
              {{ datablock3.block[2].title }}
            </p>
            <p class="bSubTitle b3__bSubTitle">
              {{ datablock3.block[2].text }}
            </p>
          </div>
        </div>
      </div>
      <joinblock class="joinblock" />
    </div>
  </div>
</template>

<script>
export default {
  buildModules: ['nuxt-animejs'],
  name: 'AboutUsPage',
  filters: {},
  components: {
    joinblock: () => import('~/components/joinBlock')
  },
  data () {
    return {
      datablock1:
      {
        block1:
        {
          title: 'О нашей компании',
          text: 'Interactivefund смогла собрать в свою команду самых передовых экспертов финансовых технологий, квалифицированных управляющих, риск-менеджеров и специалистов в среде долгосрочных инвестиций.Наш фонд работает как с частными клиентами, так и с корпоративными.'
        },
        block2:
        {
          title: 'Новая эра инвестирования',
          text: 'Наша цель – сделать работу с инвестициями и финансовыми рынками более простой и удобной, с помощью новейших технологий, которые мы внедряем в развитие систем мониторинга ситуаций на рынках и определения движения активов. Активное развитие технологий помогает просчитывать нужные объемы фундаментальной информации в течении нескольких секунд, когда большинству людей понадобится дни, а то и недели, чтобы сделать тоже самое.'
        },
        block3:
        {
          title: 'Работа с нами',
          subtitle: 'Долгосрочное инвестирование и торговля',
          text1: 'Для долгосрочных инвестиций наша команда разработала специальные портфели, с помощью которых наши клиенты могут получать стабильный пассивный доход, взвешивать риски, и выбирать самый оптимальный портфель лично под себя.',
          text2: 'Для активных трейдеров мы предоставляем многофункциональную торговую платформу с более чем 420 различными активами: валютные пары, ценные бумаги, сырьевые товары, фьючерсы, CFD контракты и другие.'
        },
        block4:
        {
          title4: 'Джордж Сорос',
          text4: 'Абсолютно не важно, прав ты или не прав. Важно лишь то, сколько денег ты зарабатываешь, когда прав, и сколько денег ты теряешь, когда ошибаешься.'
        },
        svg_blocks:
        [
          {
            value: 92,
            count: 0,
            scaleY: '22vw',
            scaleYMob: '70vw',
            target: 'svgBlock1'
          },
          {
            value: 72,
            count: 0,
            scaleY: '20vw',
            scaleYMob: '65vw',
            target: 'svgBlock2'
          },
          {
            value: 82,
            count: 0,
            scaleY: '18vw',
            scaleYMob: '60vw',
            target: 'svgBlock3'
          },
          {
            value: 76,
            count: 0,
            scaleY: '16vw',
            scaleYMob: '55vw',
            target: 'svgBlock4'
          },
          {
            value: 54,
            count: 0,
            scaleY: '14vw',
            scaleYMob: '50vw',
            target: 'svgBlock5'
          }
        ]
      },
      datablock2: {
        soros: 'Джордж Сорос',
        text: 'Абсолютно не важно, прав ты или не прав. Важно лишь то, сколько денег ты зарабатываешь, когда прав, и сколько денег ты теряешь, когда ошибаешься.'
      },
      datablock3:
      {
        block:
        [
          {
            title: 'Прозрачность',
            text: 'БЛАГОДАРЯ МНОГОЛЕТНЕМУ ОПЫТУ МЫ МОЖЕМ ОТКРЫТО ГОВОРИТЬ О НАШИХ ИНВЕСТИЦИОННЫХ ВАРИАНТАХ, КОТОРЫЕ ПРЕДОСТАВЛЯЕМ НАШИМ КЛИЕНТАМ. НАШИ ИНТЕРЕСЫ = ВАШИ ИНТЕРЕСЫ, НО С ПОПРАВКОЙ НА ФИНАНСОВО ВЫГОДНЫЕ ПОРТФЕЛИ И ИНВЕСТИЦИИ КАК ДЛЯ ВАС, ТАК И ДЛЯ НАС.'
          },
          {
            title: 'ЛИКВИДНОСТЬ',
            text: 'НАША ТОРГОВАЯ СИСТЕМА ПОДКЛЮЧЕНА К НЕСКОЛЬКИМ ПОСТАВЩИКАМ ЛИКВИДНОСТИ, ЧТО ПОЗВОЛЯЕТ ПРЕДОСТАВЛЯТЬ ВАМ САМЫЕ ТОЧНЫЕ И АКТУАЛЬНЫЕ КОТИРОВКИ ДЛЯ ПРОДУКТИВНОЙ ТОРГОВЛИ.'
          },
          {
            title: 'ЛИКВИДНОСТЬ',
            text: 'НАША ТОРГОВАЯ СИСТЕМА ПОДКЛЮЧЕНА К НЕСКОЛЬКИМ ПОСТАВЩИКАМ ЛИКВИДНОСТИ, ЧТО ПОЗВОЛЯЕТ ПРЕДОСТАВЛЯТЬ ВАМ САМЫЕ ТОЧНЫЕ И АКТУАЛЬНЫЕ КОТИРОВКИ ДЛЯ ПРОДУКТИВНОЙ ТОРГОВЛИ.'
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
  mounted () {
    window.addEventListener('scroll', this.block1ScrollEvent)
  },
  beforeDestroy () {
    window.removeEventListener('scroll', this.block1ScrollEvent)
  },
  methods: {
    block1ScrollEvent (event) {
      if ((document.querySelector('#svg_blocks').getBoundingClientRect().top <= 500) && (this.datablock1.svg_blocks[0].count === 0)) {
        this.$anime({
          targets: ['.percent__bTitle'],
          opacity: [0, 1],
          duration: 1000
        })
        // this.$anime({
        //   targets: ['#svgBlock1', '#svgBlock2', '#svgBlock3', '#svgBlock4', '#svgBlock5'],
        //   height: 0,
        //   opacity: 1,
        //   scaleY: 1
        // })
        this.datablock1.svg_blocks.forEach((item, idx) => {
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
          this.$anime({
            targets: '#' + item.target,
            height: 0,
            opacity: 1,
            scaleY: 1
          })
          this.$anime({
            targets: '#' + item.target,
            height: [0, this.mobile ? item.scaleYMob : item.scaleY],
            duration: 1000,
            easing: 'easeInOutSine'
          })
          console.log(item.name, this.mobile ? item.scaleYMob : item.scaleY)
        })
        // this.$anime({
        //   targets: '#svgBlock1',
        //   height: [0, this.datablock1.svg_blocks[0].scaleY],
        //   duration: 1000,
        //   easing: 'easeInOutSine'
        // })
        // this.$anime({
        //   targets: '#svgBlock2',
        //   // scaleY: [0, this.datablock1.svg_blocks[1].scaleY],
        //   height: [0, this.datablock1.svg_blocks[1].scaleY],
        //   duration: 1000,
        //   easing: 'easeInOutSine'
        // })
        // this.$anime({
        //   targets: '#svgBlock3',
        //   height: [0, this.datablock1.svg_blocks[2].scaleY],
        //   duration: 1000,
        //   easing: 'easeInOutSine'
        // })
        // this.$anime({
        //   targets: '#svgBlock4',
        //   height: [0, this.datablock1.svg_blocks[3].scaleY],
        //   duration: 1000,
        //   easing: 'easeInOutSine'
        // })
        // this.$anime({
        //   targets: '#svgBlock5',
        //   height: [0, this.datablock1.svg_blocks[4].scaleY],
        //   duration: 1000,
        //   easing: 'easeInOutSine'
        // })
      }
    }
  }
}
</script>

<style lang="scss" scoped>
  .about{
    .section{
       &--center{
        text-align: center;
        max-width: vwDesk(1283);
        margin: 0 auto vwDesk(200);
      }
      &--left{
        text-align: left;
        max-width: vwDesk(990);
        @media(max-width:$w-adapt){
        }
      }
      &--right{
        text-align: left;
        max-width: vwDesk(880);
        margin-bottom: vwDesk(500);
        margin-left: auto;
        @media(max-width:$w-adapt){

        }

      }
      &--marginB{
        margin-bottom: vwMob(340);
      }
      // &--marginB3{
      //   margin-bottom: vwMob(340);

      // }
      // font-family: 'Manrope', sans-serif !important;
      // & .title{
      &__bBigTitle{
        // font-style: normal !important;
        font-weight: bold !important;
        // font-size: $fs-48 !important;
        // line-height: 1 !important;

        // letter-spacing: 0.05em;
        margin-bottom: vwDesk(45);
        z-index: 2;
        &--fs18m{
          font-size: $fs-18-m;
        }
      }
      &__bSubTitle{
      // font-style: normal;
      // font-weight: normal;
      // font-size: $fs-24;
      // line-height: 1.25;
      /* or 30px */

      // letter-spacing: 0.05em;
      margin-bottom: vwDesk(20);
      z-index: 2;
      }
    }
    .b1{
      @include makeitflex(column, flex-start);
      background-image: url('~/assets/images/sheets/AboutUs/block1/background.svg');
      background-size: contain;
      padding: vwDesk(100) vwDesk(40) vwDesk(70);
      margin-top: vwDesk(190);
      z-index: 1;
      position: relative;
      @media(max-width:$w-adapt){
        padding: vhMob(48)+vhMob(20) 0 0;
        margin-top: 0;
        background-image: url('~/assets/images/sheets/AboutUs/block1/background_mob.svg');
        background-size: contain;
        background-position: top center;
      }
      &__percent{
        width: vwDesk(720);
        position: absolute;
        bottom: vwDesk(60);
        right: vwDesk(50);
        @media(max-width:$w-adapt){
          width: vwMob(350);
          right: 50%;
          transform: translateX(50%);
        }
      }
      &__cubes{
        position: absolute;
        left: 0;
        top: vwDesk(400);
        height: vwDesk(824);
        z-index: -1;
        @media(max-width:$w-adapt){
          top: vwMob(620);
          height: vwMob(260);
          left: 50%;
          transform: translateX(-50%);
          width: vwMob(335);
        }
      }
    }
    .percent {
      @include makeitflex(row, flex-start);
      &__svg{
        transform-origin: bottom;
        opacity: 0;
        transform: scaleY(0);
        @media(max-width:$w-adapt){

        }
      }
      &__bTitle{
        // font-family: 'Manrope', sans-serif !important;
        text-align: center;
        // font-style: normal !important;
        font-weight: 600 !important;
        // font-size: $fs-36 !important;
        // line-height: 49/36*1 !important;
        margin-bottom: vwDesk(60);
        opacity: 0;
        &--textFeatures{
          font-feature-settings: 'pnum' on, 'lnum' on;
          background: linear-gradient(176.05deg, #FFFFFF 34.22%, #00FDDF 101.54%, #29649B 121.84%);
          background-clip: text;
          -webkit-text-fill-color: transparent;
        }
      }
      &__col{
        @include makeitflex(column, flex-end);
        margin-right: vwDesk(48);
        @media(max-width:$w-adapt){
          width: 20%;
        }
      }
    }
    .b2{
      background-image: url('~/assets/images/sheets/AboutUs/block2/background.svg');
      background-size: cover;
      background-position-y: bottom;
      @include makeitflex(row, space-between);
      padding: 0 vwDesk(120);
      @media(max-width:$w-adapt){
        @include makeitflex(column, flex-start);
      }
      &__col{
        @include makeitflex(column, flex-start);
        position: relative;
        padding: 6vw 0 0;
      }
      &__bBigTitle{
        // font-family: 'Raleway', sans-serif !important;
        // font-style: normal !important;
        // font-weight: 800 !important;
        // font-size: $fs-48 !important;
        // line-height: 1.4;
        &--fs18m{
          font-size: $fs-18-m;
        }
      }
      &__bTitle{
        position: relative;
        // font-family: 'Raleway', sans-serif !important;
        // font-style: normal !important;
        // font-weight: bold !important;
        // font-size: $fs-36 !important;
        line-height: 1.4;
        width: vwDesk(600);
        /* or 50px */
        text-align: right;
        @media(max-width:$w-adapt){

          width: 100%;
        }
      }
      &__svg{
        position: absolute;
        width: vwDesk(20);
        @media(max-width:$w-adapt){

          width: vwMob(20);
        }
        &--1{
          left: 0;
          top: 0;
          transform: translate(200%,-100%);
          @media(max-width:$w-adapt){
            transform: translate(-40%,-100%);
          }
        }
        &--2{
          right: 0;
          bottom: 0;
          transform: translate(100%, 100% );
        }
      }
    }
    .b3{
      @include makeitflex(row,flex-start);
      margin-bottom: vwDesk(40);
      @media(max-width:$w-adapt){
        @include makeitflex(column,flex-start);
      }
      &__col{
        @include makeitflex(column, flex-start);
        width: 1/3*100%;
        border-bottom: 4px solid #14161B;
        border-top: 4px solid #14161B;
        border-left: 2px solid #14161B;
        border-right: 2px solid #14161B;
        @media(max-width:$w-adapt){
          width: 100%;
        }
      }
      &__bBigTitle{
        // font-family: 'Manrope', sans-serif !important;
        // font-style: normal !important;
        // font-weight: bold !important;
        // font-size: $fs-48  !important;
        // line-height: 1;
        /* or 47px */

        // letter-spacing: 0.05em;
        text-transform: uppercase;
        margin-bottom: vwDesk(25);
        }
      &__bSubTitle{
        // font-family: 'Manrope', sans-serif !important;
        // font-style: normal !important;
        // font-weight: 500 !important;
        // font-size: $fs-24  !important;
        // line-height: 1;
        /* or 23px */

        // letter-spacing: 0.05em;
        text-transform: uppercase;
      }
      &__block{
        width: 100%;
        padding: vwDesk(65);
        border-bottom: 4px solid #14161B;
        flex: 1;
        &:last-child{
          border-bottom: 0;
        }
      }
    }
    .joinblock{
      margin-bottom: vwDesk(150);
    }
  }
</style>
