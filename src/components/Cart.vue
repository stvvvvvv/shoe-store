<template>
    <div class="cart">
      <Cart-Item/>
    </div>
</template>
<script>
import CartItem from './CartItem.vue'

export default {
  name: 'Cart',
  components: {
    CartItem
  }
}
</script>

<style lang="scss" scoped>

</style>
