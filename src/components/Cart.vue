<template>
    <div class="cart">
      <div class="cart__img_container">
        <img class="cart__img" src="../assets/images/cart.svg" alt="Cart">
        <div
         class="cart__counter_container"
         v-if="cartLenght > 0"
         ><span class="cart__counter">{{ CartLenght }}</span></div>
      </div>
      <Cart-Item
        v-for="item in cartData"
        :key="item.article"
        :cartItemData="item"
      />
    </div>
</template>
<script>
import CartItem from './CartItem.vue'

export default {
  name: 'Cart',
  data () {
    return {
      cartLenght: 0
    }
  },
  props: {
    cartData: {
      type: Array,
      default () {
        return []
      }
    }
  },
  components: {
    CartItem
  },
  methods: { }
}
</script>

<style lang="scss" scoped>

</style>
