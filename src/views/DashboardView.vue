<template>
  這是專屬後台的頁面
    <router-link to="/back/products">後台產品列表</router-link> |
    <router-link to="/back/orders">後台訂單列表</router-link> |
    <router-link to="/">回前台首頁</router-link>

  <hr>
  <RouterView></RouterView>
</template>

<script>
import { RouterView } from 'vue-router'

export default {
  components: {
    RouterView
  }
}
</script>
