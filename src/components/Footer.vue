<template>
  <footer>
    <svg width="585" height="469" viewBox="0 0 585 469" fill="none" xmlns="http://www.w3.org/2000/svg" class="blob">
      <path d="M-81.7735 365.675C-110.077 307.15 -116.224 223.565 -80.1311 148.643C-44.0387 73.7203 35.4193 7.18511 111.336 1.05855C187.252 -5.06805 260.058 48.8971 333.241 78.9112C406.424 108.925 479.721 114.63 522.912 151.775C566.367 189.278 579.716 258.22 583.652 335.167C587.851 412.472 582.637 497.783 534.187 553.138C486.169 608.176 395.179 633.617 312.492 654.07C229.804 674.522 155.251 690.661 112.201 662.772C69.4149 635.24 57.4382 563.64 26.9139 511.148C-3.87288 458.298 -53.9019 424.517 -81.7735 365.675Z" fill="url(#paint0_linear_27_342)"/>
      <defs>
        <linearGradient id="paint0_linear_27_342" x1="723.133" y1="419.686" x2="293.576" y2="-166" gradientUnits="userSpaceOnUse">
          <stop stop-color="#73E0A9"/>
          <stop offset="1" stop-color="#5B68DF"/>
        </linearGradient>
      </defs>
    </svg>

    <div class="text">
      <h2>Chilled Grape</h2>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque eaque inventore nam odit nobis esse, aliquam omnis laboriosam earum tenetur.</p>
    </div>
    <div class="list-one">
      <h4>Company</h4>
      <p>About</p>
      <p>Careers</p>
      <p>Our work</p>
      <p>Contact</p>
    </div>
    <div class="list-two">
      <h4>Products</h4>
      <p>About</p>
      <p>Careers</p>
      <p>Our work</p>
      <p>Contact</p>
    </div>
    <div class="icons">
      <h4>Follow us</h4>
      <div>
        <span>Icon one</span>
        <span>Icon two</span>
        <span>Icon three</span>
      </div>
      <div>
        <span>Icon two</span>
        <span>Icon two</span>
        <span>Icon three</span>
      </div>
    </div>
  </footer>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
footer {
  height: 30rem;
  width: 100%;
  max-width: 2000px;
  display: flex;
  position: relative;
  align-items: flex-end;

  .blob {
    position: absolute;
    left: 0;
    bottom: 0;
  }

  .text {
    z-index: 5;
    width: 459px;
    margin: 0 auto 4rem 4rem;

    h2 {
      text-transform: uppercase;
      color: white;
      font-weight: 700;
      font-size: 36px;
      line-height: 54px;
    }

    p {
      color: white;
      font-weight: 400;
      font-size: 22px;
      line-height: 33px;
      margin: 0 0;
    }
  }

  .list-one {

    h4 {
      color: transparent;
      background: linear-gradient(to right, #73E0A9 0%, #5B68DF 100%);
      background-clip: text;
      -webkit-background-clip: text;
    }
  }

  .list-two {
    h4 {
      color: transparent;
      background: linear-gradient(to right, #73E0A9 0%, #5B68DF 100%);
      background-clip: text;
      -webkit-background-clip: text;
    }
  } 

  .icons {
    h4 {
      color: transparent;
      background: linear-gradient(to right, #73E0A9 0%, #5B68DF 100%);
      background-clip: text;
      -webkit-background-clip: text;
    }
  }
}
</style>