<template>
  <div>
    {{ count }}
  </div>
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
  }
}
</script>

<style lang="scss" scoped>

</style>