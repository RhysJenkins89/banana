<template>
  <nav>
    <h2>Chilled Grape</h2>
    <div class="item-container">
      <p>Home</p>
      <p>About</p>
      <p>Blog</p>
      <p>Pricing</p>
      <button>Login</button>
    </div>
    <div class="square" @click="toggleMenu">
      <span :class="{open: isOpen}"></span>
      <span :class="{open: isOpen}"></span>
      <span :class="{open: isOpen}"></span>
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
  background-color: transparent;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  position: absolute;

  h2 {
    text-transform: uppercase;
    margin: 0 auto 0 4rem;

    @media (max-width: 900px) {
      margin: 0 auto 0 2rem;
    }

    @media (max-width: 350px) {
      font-size: 1.2rem;
    }
  }

  .item-container {
    display: flex;
    align-items: center;
    
    @media (max-width: 850px) {
      display: none
    }

    p {
      margin: 0 0 0 2rem;
      font-weight: 600;
    }

    button {
      margin: 0 4rem;
      padding: .75rem 4rem;
      background-image: linear-gradient(to right, rgb(18, 226, 219), rgb(5, 37, 152));
      outline: none;
      border: none;
      border-radius: 10rem;
      color: white;
      font-weight: 600;

      @media (max-width: 900px) {
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

    @media (min-width: 850px) {
      display: none;
    }
  
    span {
      height: .15rem;
      width: 2rem;
      background-color: black;
      opacity: 1;
      transition: all .75s ease;
    }

    :nth-child(1).open {
      transform: translateY(.65rem) rotate(45deg);
    }

    :nth-child(2).open {
      opacity: 0;
    }

    :nth-child(3).open {
      transform: translateY(-.65rem) rotate(-45deg);
    }
  }
}
</style>