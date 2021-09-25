<template>
<div class="v-catalog-item">
  <img class="v-catalog-item__image" :src="(`src/assets/images/${product_data.image}`)" alt="img">
  <p class="v-catalog-item__name">{{product_data.name}}</p>
  <p class="v-catalog-item__price">{{product_data.price}} p.</p>
  <button
      class="v-catalog-item__add_to_card_btn btn"
      @click="sendDataToParent">
    Add to card
  </button>
</div>
</template>

<script>
export default {
  name: "v-catalog-item",
  components: {},
  props: {
    product_data: {
      type: Object,
      default() {
        return {}
      }
    }
  },
  data() {
    return {
      title: 'v-catalog-item'
    }
  },
  computed: {},
  methods: {
    sendDataToParent(){
      this.$emit('sendDataToParent', this.product_data.article)
    }
  },
  watch: {},
  mounted() {

  }
}
</script>

<style lang="scss">
.v-catalog-item {
  flex-basis: 25%;
  box-shadow: 0 0 8px 0 #e0e0e0;
  padding: .5rem;
  margin-bottom: .5rem;
  text-align: center;
  &__image {
    width: 100px;
    max-width: 100%;
  }
}

</style>