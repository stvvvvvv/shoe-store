<template>
    <nav class="nav">
        <Cart :cartData="CART"/>
    </nav>
</template>
<script>
import { mapGetters } from 'vuex'
import Cart from './Cart.vue'

export default {
  name: 'Header',
  components: {
    Cart
  },
  computed: {
    ...mapGetters([
      'CART'
    ])
  }
}
</script>
<style lang="scss">
</style>
