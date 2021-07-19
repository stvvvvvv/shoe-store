<template>
    <div class="catalog">
      <h1 class="title">Catalog</h1>
      <Loader v-if="loading"/>
      <div class="catalog__container">
        <Product-card
          v-for="product in PRODUCTS"
          :key="product.arcticle"
          :productData="product"
          @addToCart="addToCart"
        />
      </div>
    </div>
</template>

<script>
import Loader from '@/components/Loader'
import ProductCard from '@/components/ProductCard'
import { mapActions, mapGetters } from 'vuex'

export default {
  name: 'Catalog',
  data () {
    return {
      loading: true
    }
  },
  components: {
    ProductCard, Loader
  },
  methods: {
    ...mapActions([
      'GET_PRODUCTS_FROM_API',
      'ADD_TO_CART'
    ]),
    addToCart (data) {
      this.ADD_TO_CART(data)
      console.log(data)
    },
    ProductCardCounter () {
    }
  },
  computed: {
    ...mapGetters([
      'PRODUCTS'
    ])
  },
  mounted () {
    setTimeout(() => {
      this.GET_PRODUCTS_FROM_API()
      this.loading = false
    }, 1000)
  }
}
</script>

<style lang="scss"  scoped>
</style>
