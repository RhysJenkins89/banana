<template>
  <section>
    <div class="container">
      <div v-for="product in this.productData" :key="product.id">
        <ProductCard :product="product"/>
      </div>
    </div>
  </section>
</template>

<script>
import ProductCard from "./cards/ProductCard.vue"
import imageData from "../data/images.js"

export default {
  components: {
    ProductCard
  },
  data() {
    return {
      productData: {},
      images: [] 
    }
  },
  mounted() {
    this.images = imageData
    fetch("https://my-json-server.typicode.com/TomSearle/cb-devtest-api/products")
      .then(res => res.json())
      .then(data => {
        data[0].map((item) => {
          item.image = this.images[item.id - 1] 
        })
        this.productData = data[0]
      })
  }
}
</script>

<style lang="scss" scoped>
section {
  height: fit-content;
  width: 100%;
}

.container {
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  justify-items: center;
  grid-column-gap: 2.5rem;
  grid-row-gap: 3rem;

  @media (max-width: 900px) {
    grid-template-columns: 1fr 1fr;
  }

  @media (max-width: 500px) {
    grid-template-columns: 1fr;
  }
}
</style>