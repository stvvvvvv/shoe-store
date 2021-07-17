<template>
    <div class="cart">
      <div class="cart__img_container">
        <img class="cart__img" src="../assets/images/cart.svg" alt="Cart">
        <div class="cart__counter_container"><span class="cart__counter">99+</span></div>
      </div>
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
