<template>
  <div class="card">
    <img :src="product.image">
    <h3>{{product.product_name}}</h3>
    <p>{{product.price}}</p>
  </div>
</template>

<script>
export default {
  props: ["product"]
}
</script>

<style lang="scss" scoped>
.card {
  height: 25rem;
  width: 20rem;
  box-shadow: 0rem 0rem 1.5rem rgba(0, 0, 0, .5);
  border-radius: 1.5rem;

  @media (max-width: 500px) {
    width: 10rem;
  }

  img {
    height: 70%;
    width: 100%;
    object-fit: cover;
    border-radius: 1.5rem;
    box-shadow: 0rem 1rem 1.5rem -1rem rgba(0, 0, 0, .5);
  }
}
</style>