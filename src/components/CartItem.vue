<template>
    <div class="cart-item">
      <div class="cart-item__img_container">
          <img class="cart-item__img" :src=" require('../assets/images/' + cartItemData.image) " alt="Sneakers"/>
        </div>
        <div class="cart-item__information">
          <h3 class="cart-item__name">{{ cartItemData.name }}</h3>
          <p class="cart-item__id">{{ cartItemData.article }}</p>
          <p class="cart-item__price">{{ cartItemData.price }} ₽</p>
          <p class="cart-item__counter"></p>
          <div class="cart-item__btn_container">
            <button>Delete</button>
          </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'CartItem',
  props: {
    cartItemData: {
      type: Object,
      default () {
        return {}
      }
    }
  }
}
</script>

<style lang="scss">
</style>
