<template>
  <section>
    <!-- Text section -->
    <div class="text-section">
      <h2>Lorem ipsum dolor sit <br> amet.</h2>
      <p>Labore proident cupidatat quis commodo commodo proident ex cupidatat ea qui sint minim. Tempor veniam tempor est non voluptate dolor quis id consectetur velit commodo. Eiusmod nulla sint sit non aute cupidatat adipisicing dolor veniam sint tempor excepteur reprehenderit.</p>
      <button>Read more</button>
    </div>

    <!-- Plant section -->
    <div class="image-section">
      <svg width="578" height="528" viewBox="0 0 578 528" fill="none" xmlns="http://www.w3.org/2000/svg" class="blob">
        <path d="M460.111 75.7686C506.768 95.8054 553.155 142.745 570.159 207.059C587.163 271.373 574.259 353.83 532.547 398.094C490.835 442.358 420.221 448.851 361.637 469.937C303.052 491.024 256.836 526.778 212.32 527.547C167.467 528.242 124.315 493.951 82.6293 449.818C40.6052 405.611 0.0470156 351.561 0.35209 292.399C0.564022 233.658 41.301 169.73 79.6848 113.238C118.069 56.7456 153.854 7.19349 193.551 0.939082C232.909 -5.39008 276.61 31.2318 321.493 46.4562C366.713 61.7554 413.547 55.3105 460.111 75.7686Z" fill="url(#paint0_linear_282_240)"/>
        <defs>
          <linearGradient id="paint0_linear_282_240" x1="-43" y1="473.594" x2="510.347" y2="595.899" gradientUnits="userSpaceOnUse">
            <stop stop-color="#73E0A9"/>
            <stop offset="1" stop-color="#5B68DF"/>
          </linearGradient>
        </defs>
      </svg>
      <img src="../assets/images/plant.png" class="image">
    </div>
  </section>
  
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>  
section {
  height: 110vh;
  width: 100%;
  max-width: 2000px;
  display: grid;
  grid-template-columns: 1fr 1fr;
  place-items: center;

  @media (max-width: 1200px) {
    height: fit-content;
    grid-template-columns: 1fr;
    grid-template-rows: 1fr 1fr;
  }

  .text-section {
    margin: 4rem 6rem;

    @media (max-width: 1200px) {
      margin: 4rem 8rem;
    }

    @media (max-width: 1000px) {
      margin: 4rem 6rem;
    }

    @media (max-width: 500px) {
      margin: 4rem 2rem;
    }

    h2 {
      text-transform: uppercase;
      font-size: 36px;
      margin: 0 0 3rem 0;
      line-height: 54px;
      font-weight: 700;
    }

    p {
      font-size: 24px;
      line-height: 36px;
      margin: 0 0 3rem 0;
    }

    button {
      margin: 0 0;
      padding: .75rem 4rem;
      background-image: linear-gradient(90deg, #73E0A9 0%, #5B68DF 100%);
      outline: none;
      border: none;
      border-radius: 10rem;
      color: white;
      font-weight: 600;
      font-size: 16px;
    }
  }

  .image-section {
    position: relative;

    @media (max-width: 1200px) {
      grid-row-start: 1;
    }

    .blob {
      margin-top: 10rem;
      
      @media (max-width: 600px) {
        width: 90vw;
      }
    }

    .image {
      height: 789px;
      width: 524px;
      object-fit: contain;
      position: absolute;
      top: -20%;
      left: 0;

      @media (max-width: 600px) {
        width: 90vw;
      }

      @media (max-width: 450px) {
        top: -15%;
      }

      @media (max-width: 350px) {
        top: -10%;
      }
    }
  }
}
</style>