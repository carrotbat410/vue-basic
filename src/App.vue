<template>
  <div>{{ count }}</div>
  <h1>Vue.js 라이플사이클 테스트</h1>
</template>

<script>
export default {
  data() {
    return {
      count: 0,
    }
  },
  beforeCreate() {
    console.log("LifeCycle is beforeCreate", this.count)
  },
  created() {
    console.log("LifeCycle is created", this.count)
  },
  beforeMount() {
    console.log("LifeCycle is beforeMount", document.querySelector('h1'))
  },
  mounted() {
    console.log("LifeCycle is mounted", document.querySelector('h1'))
  },
  methods: {
    test() {
      console.log("테스트 함수 호출")
    }
  }
}
</script>

<style lang="scss" scoped>

</style>