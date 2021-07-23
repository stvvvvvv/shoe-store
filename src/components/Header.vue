<template>
    <nav class="nav">
        <cart
        :cartData="CART"
        />
        <favorites />
    </nav>
</template>
<script>
import { mapGetters } from 'vuex'
import Cart from './Cart'
import Favorites from './Favorites'

export default {
  name: 'Header',
  data () {
    return {
    }
  },
  components: {
    Cart, Favorites
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
