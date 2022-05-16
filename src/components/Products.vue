<template>
  <section>
    <div class="container" v-if="!showAllData">
      <div v-for="product in this.productData.slice(0, 6)" :key="product.id">
        <ProductCard :product="product"/>
      </div>
    </div>
    <div class="container" v-else>
      <div v-for="product in this.productData" :key="product.id">
        <ProductCard :product="product"/>
      </div>
    </div>
    <div class="text-grid">
      <div>
        <p @click="showAllData = !showAllData">
          <span v-if="!showAllData">Load more</span>  
          <span v-else>Show fewer</span>  
        </p>
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
      productData: [],
      images: [],
      showAllData: false
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
  max-width: 2000px;

  .text-grid {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    justify-items: center;

    div {
      grid-column-start: 1;
      width: 369px;

      p {
        font-weight: 600;
        font-size: 24px;
        line-break: 36px;
        color: #5C6DDE;
        margin-top: 4rem;
      }
    }
  }
}

.container {
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  justify-items: center;
  grid-row-gap: 4rem;

  @media (max-width: 900px) {
    grid-template-columns: 1fr 1fr;
  }

  @media (max-width: 500px) {
    grid-template-columns: 1fr;
    justify-items: flex-start;
  }
}
</style>