<template>
  <div>
    <MyHeader title="淘宝购物车" background="tomato" color="#fff" />
    <div class="main">
      <MyGoods v-for="item in list" :key="item.goods_id" :list="item" />
    </div>
    <MyFooter />
  </div>
</template>

<script>
import MyHeader from '@/components/MyHeader.vue'
import MyGoods from '@/components/MyGoods.vue'
import MyFooter from '@/components/MyFooter.vue'
import axios from 'axios'
export default {
  components: {
    MyHeader,
    MyGoods,
    MyFooter
  },
  data() {
    return {
      list: []
    }
  },
  methods: {
    async getlist() {
      const res = await axios({ url: '/api/cart' })
      // console.log(res)
      this.list = res.data.list
      // console.log(this.list)
    }
  },
  created() {
    this.getlist()
  }
}
</script>

<style scoped>
.main {
  padding: 50px 0;
}
</style>
