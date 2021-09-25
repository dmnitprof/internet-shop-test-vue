<template>
<div class="v-main-wrapper">
  <v-catalog/>
  <v-cart/>
</div>
</template>

<script>
import vCatalog from './v-catalog.vue'
import vCart from './v-cart.vue'

export default {
  name: "v-main-wrapper",
  components: {
    vCart,
    vCatalog
  },
  props: {},
  data() {
    return {

    }
  },
  computed: {},
  methods: {},
  watch: {},
  mounted() {

  }
}
</script>

<style lang="scss">
.v-main-wrapper{
  max-width: 1140px;
  margin: 0 auto;
}
</style>