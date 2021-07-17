<template>
    <div class="catalog">
      <h1 class="title">Catalog</h1>
      <div class="catalog__container">
        <Product-card
          v-for="product in PRODUCTS"
          :key="product.arcticle"
          :productData="product"
        />
      </div>
    </div>
</template>

<script>
import ProductCard from '@/components/ProductCard'
import { mapActions, mapGetters } from 'vuex'

export default {
  name: 'Catalog',
  components: {
    ProductCard
  },
  methods: {
    ...mapActions([
      'GET_PRODUCTS_FROM_API'
    ])
  },
  computed: {
    ...mapGetters([
      'PRODUCTS'
    ])
  },
  mounted () {
    this.GET_PRODUCTS_FROM_API()
  }
}
</script>

<style lang="scss"  scoped>
</style>
