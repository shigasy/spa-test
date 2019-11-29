<template>
  <div>
    <h1>test</h1>
    <h1>ここテストでるよ</h1>
    <h1>kokotestderuyo</h1>
    <h1>test</h1>
    <h1>ここテストでるよ</h1>
    <h1>kokotestderuyo</h1>
    <h1>test</h1>
    <h1>ここテストでるよ</h1>
    <h1>kokotestderuyo</h1>
    <h1>test</h1>
    <h1>ここテストでるよ</h1>
    <h1>kokotestderuyo</h1>
    <button
      @click="getMsg"
    >
      Hello
    </button>
    <nuxt-link to="/">
      Home page
    </nuxt-link>
    {{ msg }}
    {{ msg2 }}
  </div>
</template>

<script>
export default {
  data: () => ({
    msg: '',
    msg2: ''
  }),
  created () {
    this.getMsg2()
  },
  methods: {
    getMsg () {
      this.$axios.$get('/api/v1/hello').then(res => (this.msg = res.msg))
    },
    getMsg2 () {
      this.$axios.$get('/api/v1/hello').then(res => (this.msg2 = res.msg))
    }
  }
}
</script>
