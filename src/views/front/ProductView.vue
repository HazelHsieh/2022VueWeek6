<template>
  這是單一產品頁面
  <h2>{{ product.title }}</h2>
  <img :src="product.imageUrl" class="img-fluid" alt="">
</template>

<script>
const { VITE_APP_URL, VITE_PATH } = import.meta.env
export default {
  data () {
    return {
      product: {}
    }
  },
  methods: {
    getProduct () {
      console.log(this.$route.params)
      const { id } = this.$route.params
      this.$http.get(`${VITE_APP_URL}api/${VITE_PATH}/product/${id}`)
        .then(res => {
          this.product = res.data.product
        })
    }
  },
  mounted () {
    this.getProduct()
  }
}
</script>
