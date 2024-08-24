<template>
  <div>{{ rawHtml }}</div>
  <div>{{ rawHtml2 }}</div>
  <div v-html="rawHtml2"></div>

  <!-- 클래스 명시 방법 -->
  <h2 v-bind:class = "{active: isActive}">클래스 바인딩 테스트입니다.</h2>
  <!-- 클래스 명시 방법 축약형 -->
  <h2 :class="{ active: isActive }">클래스 바인딩 테스트입니다.</h2>

  <button @click="change">버튼</button>
</template>

<script>
export default {
  data() {
    return {
      rawHtml: '이것은 텍스트 문구입니다.',
      rawHtml2: '<span style="color: red">이것은 빨간색이어야 합니다</span>',
      isActive: false,
      
    }
  },
  methods: {
    change() {
      this.isActive = !this.isActive
    },
  }
}
</script>

<style scoped>
h2.active {
  color: green;
}
</style>