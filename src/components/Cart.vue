<template>
    <div class="cart">
      <div class="cart__img_container">
        <img
        class="cart__img"
        src="../assets/images/cart.svg"
        alt="Cart"
        @click="showCartItems = !showCartItems"
        >
        <div
         class="cart__counter_container"
         v-if="cartData.length > 0"
        >
          <span class="cart__counter">
            {{ cartData.length }}
          </span>
        </div>
      </div>
      <div class="cart-item__wrapper " :class="{ active: showCartItems }">
        <h2
        class="cart-item__empty"
        v-if="cartData.length == 0"
        >
          You cart is empty :( <br>
          But you can fill it right now! <br>
          <a href="#">Click here!</a>
        </h2>
        <div
        class="cart-item__info"
        v-else
        >
          <h1>Total</h1>
          <h2>Sub-total: </h2>
          <div class="delivery__container">
            <h2 class="delivery__title">
              Delivery
            </h2>
            <div class="delivery__select-container">
              <select name="deliverySelect" id="deliverySelect">
                <option value="0">Standard delivery</option>
                <option value="1">Express delivery</option>
                <option value="2">Delivery to the pickup point</option>
            </select>
            </div>
          </div>
          <button class="cart-item__pay-btn">
            Pay
          </button>
        </div>
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
      showCartItems: false,
      noScroll: false
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
