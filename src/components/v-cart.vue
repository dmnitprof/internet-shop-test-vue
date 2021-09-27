<template>
<div class="v-card">
  <h3>Cart</h3>
 <v-cart-item
     v-for="(item, index) in cart_data"
     :key="item.article"
     :cart_item_data="item"
     :deleteFromCart="deleteFromCart(index)"
 />
</div>
</template>

<script>
import vCartItem from './v-cart-item.vue'
export default {
  name: "v-cart",
  components: {vCartItem},
  props: {
    cart_data: {
      type: Array,
      default() {
        return {}
      }
    }
  },
  data() {
    return {
      title: 'v-cart'
    }
  },
  computed: {},
  methods: {
    deleteFromCart(index) {
     console.log(index)
    }
  },
  watch: {},
  mounted() {

  }
}
</script>

<style scoped>
.v-card {
  text-align: center;
}
</style>