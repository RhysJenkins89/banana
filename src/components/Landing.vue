<template>
  <section>
    <div class="header-container">
      <h1>Lorem ipsum</h1> 
      <h1>dolor sit amet.</h1>
      <button>Read More</button>
    </div>  
  </section>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
section {
  height: 120vh;
  width: 100%;
  display: flex;
  align-items: center;

  .header-container {
    margin: 0 0 0 20rem;

    @media (max-width: 1000px) {
      margin: 0 6rem;
    }

    @media (max-width: 500px) {
      margin: 0 4rem;
    }

    @media (max-width: 350px) {
      margin: 0 2rem;
    }

    h1 {
      text-transform: uppercase;
      margin: 0 0;
      font-size: 3.25rem;
    
      @media (max-width: 500px) {
        font-size: 3rem;
      }
    }

    button {
      margin: 1.25rem 0;
      padding: 1rem 4rem;
      background-image: linear-gradient(to right, rgb(18, 226, 219), rgb(5, 37, 152));
      outline: none;
      border: none;
      border-radius: 10rem;
      color: white;
      font-weight: 600;
      font-size: 1rem;
    }
  }
}
</style>