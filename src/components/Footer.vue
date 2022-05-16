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
      <div class="container">
        <div class="icon-container">
          <TelegramIcon />
        </div>
        <div class="icon-container" style="place-self: center;">
          <TwitterIcon />
        </div>
        <div class="icon-container" style="place-self: flex-end;">
          <YouTubeOuterIcon style="grid-column: 1; grid-row: 1;"/>
          <YouTubeInnerIcon style="grid-column: 1; grid-row: 1;"/>
        </div>
        <div class="icon-container">
          <FacebookOuterIcon style="grid-column: 1; grid-row: 1;"/>
          <FacebookInnerIcon style="grid-column: 1; grid-row: 1;"/>
        </div>
        <div class="icon-container" style="place-self: center;">
          <InstaOuterIcon style="grid-column: 1; grid-row: 1;"/>
          <InstaInnerIcon style="grid-column: 1; grid-row: 1;"/>
          <InstaDotIcon style="grid-column: 1; grid-row: 1; margin: 0 0 13px 12px"/>
        </div>
        <div class="icon-container" style="place-self: flex-end;">
          <TikTokIcon />
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import {
  TelegramIcon, 
  TwitterIcon, 
  YouTubeOuterIcon, 
  YouTubeInnerIcon, 
  FacebookOuterIcon, 
  FacebookInnerIcon, 
  InstaOuterIcon,
  InstaInnerIcon,
  InstaDotIcon,
  TikTokIcon
} from "../assets/icons/icons.js"

export default {
  components: {
    TelegramIcon,
    TwitterIcon,
    YouTubeOuterIcon,
    YouTubeInnerIcon,
    FacebookOuterIcon,
    FacebookInnerIcon,
    InstaOuterIcon,
    InstaInnerIcon,
    InstaDotIcon,
    TikTokIcon
  }
}
</script>

<style lang="scss" scoped>
footer {
  height: 30rem;
  width: 100%;
  max-width: 2000px;
  position: relative;
  display: flex;
  align-items: flex-end;

  h4 {
    font-weight: 500;
    font-size: 20px;
    line-height: 30px;
    color: transparent;
    background: linear-gradient(to right, #73E0A9 0%, #5B68DF 100%);
    background-clip: text;
    -webkit-background-clip: text;

    @media (max-width: 1300px) {
      color: #212121;
    }
  }

  p {
    font-weight: 400;
    font-size: 18px;
    line-height: 27px;
  }

  .blob {
    position: absolute;
    left: 0;
    bottom: 0;

    @media (max-width: 600px) {
      width: 90vw;
    }
  }

  .text {
    z-index: 1;
    width: 459px;
    margin: 0 auto 4rem 4rem;

    @media (max-width: 900px) {
      margin: 0 auto 4rem 2rem;
    }

    h2 {
      text-transform: uppercase;
      color: white;
      font-weight: 700;
      font-size: 36px;
      line-height: 54px;

      @media (max-width: 1300px) {
        margin: 0 0;
      }

      @media (max-width: 450px) {
        font-size: 1.75rem;
      }

      @media (max-width: 350px) {
        font-size: 1.4rem;
      }
    }

    p {
      color: white;
      font-weight: 400;
      font-size: 22px;
      line-height: 33px;
      margin: 0 0;

      @media (max-width: 1300px) {
        display: none;
      }
    }
  }

  .list-one {
    width: 211px;
    margin: 4rem 0;
    z-index: 5;

    @media (max-width: 900px) {
      display: none;
    }
    
    p:last-child {
      margin-bottom: 0;
    }
  }

  .list-two {
    width: 211px;
    margin: 4rem 0;
    z-index: 5;

    @media (max-width: 900px) {
      display: none;
    }

    p:last-child {
      margin-bottom: 0;
    }
  } 

  .icons {
    width: 211px;
    height: 245.2px;
    margin: 4rem 4rem 4rem 0;
    z-index: 1;
    
    @media (max-width: 900px) {
      display: flex;
      flex-direction: column;
      justify-content: flex-end;
      margin: 4rem 2rem 4rem 0;
    }

    @media (max-width: 650px) {
      display: none;
    }

    .container {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      grid-row-gap: 1.2rem;

      .icon-container {
        height: 45px;
        width: 45px;
        border-radius: 8px;
        background: linear-gradient(to right, #73E0A9 0%, #5B68DF 100%);
        display: grid;
        place-items: center;

        @media (max-width: 800px) {
          outline: 1px solid white;
        }
      }
    }
  }
}
</style>