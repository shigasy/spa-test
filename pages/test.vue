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
    {{ msg }}
    <nuxt-link to="/">
      Home page
    </nuxt-link>
  </div>
</template>

<script>
export default {
  data: () => ({
    msg: '',
    msg2: ''
  }),
  methods: {
    getMsg () {
      this.$axios.$get('/api/v1/hello').then(res => (this.msg = res.msg))
    }
  }
}
</script>
