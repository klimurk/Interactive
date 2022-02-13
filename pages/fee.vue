<template>
  <div>
    <div class="">
      1213213
    </div>
    <form-card :id.sync="id" title="nazvanie" @submit="func" />
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  components: {
    formCard: () => import('~/components/card')
  },
  layout: 'error',
  data () {
    return {
      id: 0,
      customer: {
        id: 25,
        text: 'sdsdsd'
      }
    }
  },
  watch: {
    id (value) {
      console.log(value)
    },
    customer: {
      deep: true,
      handler (obj) {
        console.log(obj)
      }
    }
  },
  created () {
    console.log('created')
    this.$dark = false
  },
  mounted () {
    console.log('mounted')
  },
  methods: {
    func () {

    }
  }
}
</script>
