<template>
  <div class="card">
    <img :src="product.image">
    <h3>{{product.product_name}}</h3>
    <p>£{{product.price}}</p>
  </div>
</template>

<script>
export default {
  props: ["product"]
}
</script>

<style lang="scss" scoped>
.card {
  height: 440px;
  width: 369px;
  box-shadow: 0rem 4px 20px rgba(0, 0, 0, .15);
  border-radius: 30px;

  @media (max-width: 950px) {
    width: 300px;
    height: fit-content;
    padding-bottom: 1rem;
  }

  @media (max-width: 500px) {
    width: 80vw;
    height: fit-content;
    margin: 0 0;
  }

  img {
    height: 314px;
    width: 100%;
    object-fit: cover;
    border-radius: 1.5rem;
    box-shadow: 0 8px 20px rgba(0, 0, 0, .25);
  }

  h3 {
    text-transform: uppercase;
    font-size: 24px;
    line-height: 36px;
    font-weight: 700; 
    color: #212121;
    margin: 1.25rem 0 .25rem 1.5rem;

    @media (max-width: 950px) {
      margin: 1.25rem 1.5rem .25rem 1.5rem;
    }
  }

  p {
    font-size: 24px;
    line-height: 36px;
    font-weight: 700; 
    color: #747474;
    margin: 0 0 0 1.5rem;
  }
}
</style>