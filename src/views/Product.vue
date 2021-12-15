<template>
 <main class="wrapper">
        <h1>Products</h1>

        <div class="card-container">
          <Productcard
              v-for="(product, index)  in inventory"
              :key="product.id"
              :index="index"
              :product="product"
              :addToCart="addToCart"
              class="card">
          </Productcard>
        </div>
      </main>
</template>

<script>
import Productcard from '@/components/Productcard.vue'
export default {
  name: 'Product',
  props: ['inventory', 'addToCart'],
  components: {
    Productcard
  }
}
</script>
