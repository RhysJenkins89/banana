<template>
  <nav>
    <!-- Main nav -->
    <h2>Chilled Grape</h2>
    <div class="item-container">
      <p>Home</p>
      <p>About</p>
      <p>Blog</p>
      <p>Pricing</p>
      <button>Login</button>
    </div>

    <!-- Hamburger -->
    <div class="square" :class="{open: isOpen}" @click="toggleMenu">
      <span :class="{open: isOpen}"></span>
      <span :class="{open: isOpen}"></span>
      <span :class="{open: isOpen}"></span>
    </div>

    <!-- Overlay -->
    <div class="overlay" :class="{open: isOpen}" @click="toggleMenu"></div>

    <!-- Slide-out menu -->
    <div class="slide-out-menu" :class="{open: isOpen}">
      <p>Home</p>
      <p>About</p>
      <p>Blog</p>
      <p>Pricing</p>
      <button>Login</button>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false
    } 
  },
  methods: {
    toggleMenu() {
      this.isOpen = !this.isOpen
    }
  }
}
</script>

<style lang="scss" scoped>
nav {
  height: 5rem;
  width: 100%;
  max-width: 2000px;
  background-color: transparent;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  position: absolute;
  z-index: 5;

  h2 {
    text-transform: uppercase;
    margin: 0 auto 0 4rem;
    color: white;
    font-size: 36px;
    font-weight: 700;

    @media (max-width: 900px) {
      margin: 0 auto 0 2rem;
    }

    @media (max-width: 450px) {
      font-size: 1.75rem;
    }

    @media (max-width: 350px) {
      font-size: 1.4rem;
    }
  }

  .item-container {
    display: flex;
    align-items: center;
    
    @media (max-width: 875px) {
      display: none
    }

    p {
      margin: 0 0 0 2rem;
      font-weight: 600;
      font-size: 16px;
    }

    button {
      margin: 0 4rem;
      padding: .75rem 4rem;
      background-image: linear-gradient(90deg, #73E0A9 0%, #5B68DF 100%);;
      outline: none;
      border: none;
      border-radius: 10rem;
      color: white;
      font-weight: 600;
      font-size: 16px;

      @media (max-width: 1000px) {
        margin: 0 2rem;
      }
    }
  }

  .square {
    margin: 0 2rem;
    height: 2.5rem;
    width: 2.5rem;
    background-color: transparent;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
    cursor: pointer;
    z-index: 25;

    &.open {
      position: fixed;
    }

    @media (min-width: 875px) {
      display: none;
    }
  
    span {
      height: .15rem;
      width: 2rem;
      background-color: black;
      opacity: 1;
      transition: all .75s ease;

      @media (max-width: 550px) {
        background-color: white;
      }
    }

    :nth-child(1).open {
      transform: translateY(.65rem) rotate(45deg);
      background-color: black;
    }

    :nth-child(2).open {
      opacity: 0;
      background-color: black;
    }

    :nth-child(3).open {
      transform: translateY(-.65rem) rotate(-45deg);
      background-color: black;
    }
  }

  .overlay {
    position: fixed;
    top: 0;
    left: 0;
    height: 100vh;
    width: 100vw;
    background-color: rgba(0, 0, 0, .5);
    opacity: 0;
    visibility: hidden;
    transition: all .75s ease;
    z-index: 15;

    &.open {
      opacity: 1;
      visibility: visible;
    }
  }

  .slide-out-menu {
    position: fixed;
    top: 0;
    right: 0;
    height: 100vh;
    width: 17.5rem;
    background-color: white;
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    visibility: hidden;
    transform: translateX(17.5rem);
    transition: all 1s ease;
    z-index: 20;

    &.open {
      visibility: visible;
      transform: translateX(0rem);
    }

    p {
      margin: 1rem 2rem;
      font-weight: 600;
      font-size: 1.25rem; 
    
      &:first-child {
        margin-top: 6rem;
      }
    }

    button {
      margin: auto 2rem 2rem 0;
      padding: .75rem 4rem;
      background-image: linear-gradient(90deg, #73E0A9 0%, #5B68DF 100%);
      outline: none;
      border: none;
      border-radius: 10rem;
      color: white;
      font-weight: 600;

      @media (max-width: 900px) {
        margin: auto 2rem 2rem 0;
      }
    }
  }
}
</style>