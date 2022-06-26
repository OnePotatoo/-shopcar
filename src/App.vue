<template>
  <div>
    <MyHeader title="淘宝购物车" background="tomato" color="#fff" />
    <div class="main">
      <MyGoods />
    </div>
    <MyFooter />
  </div>
</template>

<script>
import MyHeader from '@/components/MyHeader.vue'
import MyGoods from '@/components/MyGoods.vue'
import MyFooter from '@/components/MyFooter.vue'
export default {
  components: {
    MyHeader,
    MyGoods,
    MyFooter
  }
}
</script>

<style scoped>
.main {
  padding: 50px 0;
}
</style>
