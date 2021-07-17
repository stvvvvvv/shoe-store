<template>
<main class="wrapper">
  <Cart/>
  <Catalog/>
</main>
</template>

<script>
import Catalog from '@/components/Catalog'
import Cart from '@/components/Cart'

export default {
  name: 'Wrapper',
  components: {
    Catalog,
    Cart
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
</style>
