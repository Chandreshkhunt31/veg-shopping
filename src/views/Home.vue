<template>
  <div class="home">
     <div class="splash-container">
        <div class="splash">
          <h1>Splendid Food</h1>
        </div>
      </div>

      <main class="wrapper">

        <h2>Recommended</h2>

        <div class="recommended">

          <Productcard
              v-for="(product, index)  in inventory.slice(0,3)"
              :key="product.id"
              :index="index"
              :product="product"
              :addToCart="addToCart"
              class="card">
          </Productcard>
        </div>

      </main>
  </div>
</template>

<script>
import Productcard from '@/components/Productcard.vue'
export default {
  name: 'Home',
  props: ['inventory', 'addToCart'],
  components: {
    Productcard
  }
}
</script>
