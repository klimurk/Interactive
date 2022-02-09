<template>
  <div>
    <div class="">1213213 </div>
    <form-card title="nazvanie" :id.sync="id" @submit="func"></form-card>

  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  layout: 'error',
  components: {
    formCard: () => import('~/components/card')
  },
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
