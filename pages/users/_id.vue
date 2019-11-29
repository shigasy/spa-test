<template>
  <div>
    <h1>test</h1>
    <h1>ここテストでるよ</h1>
    <h1>kokotestderuyo</h1>
    <button
      @click="getMsg"
    >
      Hello
    </button>
    {{ msg }}
    {{ msg2 }}
    {{ $route.params.id }}
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
