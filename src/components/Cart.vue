<template>
    <div class="cart">
      <div class="cart__img_container">
        <img class="cart__img" src="../assets/images/cart.svg" alt="Cart">
        <div
         class="cart__counter_container"
         v-if="cartLenght > 0"
         ><span class="cart__counter">{{ CartLenght }}</span></div>
      </div>
      <div class="cart-item__wrapper">
        <Cart-Item
        v-for="(item, index) in cartData"
        :key="item.article"
        :cartItemData="item"
        @delFromCart="delFromCart(index)"
        />
      </div>
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
  methods: {
    delFromCart (index) {
      console.log(index)
    }
  }
}
</script>

<style lang="scss" scoped>

</style>
