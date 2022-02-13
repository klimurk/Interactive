<template>
  <div>
    <v-img
      class="pageImgHead"
      lazy-src="/assets/images/sheets/AccountsType/head.png"
      :src="require('/assets/images/sheets/AccountsType/head.png')"
      width="96%"
      alt=""
    />
    <div class="info_block">
      <p class="title">
        Сигналы
      </p>
      <iframe src="http://pay.t247.win/widgets/tehnicheskie-indikatory/" frameborder="0" />
    </div>
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
    }
  }
}

</script>
<style lang="scss" scoped>
.info_block{
  padding: 0 130px;
  .title{
    font-family: 'Manrope', sans-serif !important;
    font-style: normal !important;
    font-size: $h2FS !important;
    line-height: 1;
    letter-spacing: 0.05em !important;
    font-weight: 800 !important;
    text-transform: uppercase;

    text-align: center;
  }
  & >iframe{
    margin: 70px 0 ;
    width: 100%;
    height: 542/1920*100vw;
  }
}
</style>
