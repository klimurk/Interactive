<template>
  <div>
    <v-img
      class="pageImgHead"
      lazy-src="/assets/images/sheets/Analytic/head.png"
      :src="require('/assets/images/sheets/Analytic/head.png')"
      width="96%"
      alt=""
    />
    <template v-for="block in datablock">
      <div v-if="block.condition == $route.params.instrument" :key="block.condition" class="instrumentPage">
        <div v-for="iframe in block.iframes" :key="iframe.title" class="instrumentPage_inner">
          <p class="title">
            {{ iframe.title }}
          </p>
          <iframe :src="iframe.iframeLink" frameborder="0" />
        </div>
      </div>
    </template>
  </div>
</template>

<script>
// import Template from '../template.vue'
// import Template from '~/pages/template.vue'
export default {
  buildModules: ['nuxt-animejs'],
  name: 'InstrumentPage',
  filters: {},
  components: {
    // Template
    // Template
    // joinblock: () => import('~/components/joinBlock')
  },
  data () {
    return {

      datablock:
      [
        {
          condition: 'analytic',
          iframes:
          [
            {
              title: 'Опорные уровни',
              iframeLink: ''
            }
          ]
        },
        {
          condition: 'trader',
          iframes:
          [
            {
              title: 'Опорные уровни',
              iframeLink: ''
            }
          ]
        },
        {
          condition: 'informers',
          iframes:
          [
            {
              title: 'Опорные уровни',
              iframeLink: ''
            }
          ]
        },
        {
          condition: 'calendars',
          iframes:
          [
            {
              title: 'Опорные уровни',
              iframeLink: ''
            }
          ]
        },
        {
          condition: 'signals',
          iframes:
          [
            {
              title: 'Опорные уровни',
              iframeLink: 'http://pay.t247.win/widgets/tehnicheskie-indikatory/'
            }
          ]
        },
        {
          condition: 'calendar',
          iframes:
          [
            {
              title: 'Опорные уровни',
              iframeLink: ''
            }
          ]
        }
      ]
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
.instrumentPage{
  margin: 70/1920*100vw 125/1920*100vw ;
  .title{
    font-family: 'Manrope', sans-serif !important;
    font-style: normal !important;
    font-weight: 800 !important;
    font-size: $h2FS !important;
    line-height: 100%;
    /* or 48px */

    letter-spacing: 0.05em !important;
    text-transform: capitalize;
    text-align: center;
    margin-bottom: 80/1920*100vw;
  }
  & iframe{
    width: 100%;
    min-height: 550/1920*100vw;
  }
}
</style>
