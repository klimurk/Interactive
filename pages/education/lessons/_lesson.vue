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
      <div v-if="block.condition == $route.params.lesson" :key="block.condition" class="instrumentPage">
        <p class="title">
          {{ block.title }}
        </p>
        <div v-for="group in block.blocks" :key="group.title" class="videoBlock">
          <p class="gtitle">
            {{ group.title }}
          </p>
          <div
            class="videos"
          >
            <div
              v-for="video in group.videos"
              :key="video.name"
              class="vidblock"
            >
              <iframe
                :src="video.url"
                title="YouTube video player"
                frameborder="0"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                allowfullscreen
              />
              <p class="text">
                {{ video.name }}
              </p>
            </div>
          </div>
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
          condition: 'beginner',
          title: 'Начинающим',
          blocks:
          [
            {
              title: 'Введение',
              videos:
              [
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                }
              ]
            },
            {
              title: 'Терминология',
              videos:
              [
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                }
              ]
            },
            {
              title: 'Ошибки',
              videos:
              [
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                }
              ]
            }
          ]
        },
        {
          condition: 'advanced',
          title: 'Продвинутым',
          blocks:
          [
            {
              title: 'Фундаментальный анализ',
              videos:
              [
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                }
              ]
            },
            {
              title: 'Технический анализ',
              videos:
              [
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                }
              ]
            },
            {
              title: 'Индикаторы',
              videos:
              [
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                }
              ]
            }
          ]
        },
        {
          condition: 'crypto',
          title: 'Криптовалюта',
          blocks:
          [
            {
              title: 'Фундаментальный анализ',
              videos:
              [
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                }
              ]
            },
            {
              title: 'Технический анализ',
              videos:
              [
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                }
              ]
            },
            {
              title: 'Индикаторы',
              videos:
              [
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                },
                {
                  name: '',
                  url: 'https://www.youtube.com/embed/dJP7lu9gXjc'
                }
              ]
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
  margin: vwDesk(70) vwDesk(210) ;
  .title{
    font-family: 'Manrope', sans-serif !important;
    font-style: normal !important;
    font-weight: 800 !important;
    font-size: $fs-48 !important;
    line-height: 100%;
    /* or 48px */
    letter-spacing: 0.05em !important;
    text-transform: capitalize;
    text-align: center;
    margin-bottom: vwDesk(80);
  }
  .videoBlock{
    .gtitle{
      font-family: 'Manrope', sans-serif !important;
      font-style: normal !important;
      font-weight: 600 !important;
      font-size: $fs-64  !important;
      line-height: 87/64*1;
      margin-bottom: vwDesk(120);
    }
    .videos{
      margin: 0 vwDesk(130);
      @include makeitflex(row, flex-start);
      flex-wrap: wrap;
      .vidblock{
        width: 1/3*100%;
        padding: 0 vwDesk(40);
        margin-bottom: vwDesk(120);
        iframe{
          height: vwDesk(400);
          width: 100%;
        }
      }
    }
  }
}
</style>
