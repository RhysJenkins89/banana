<template>
  <nav>
    <h2>Chilled Grape</h2>
    <p>Home</p>
    <p>About</p>
    <p>Blog</p>
    <p>Pricing</p>
    <button>Login</button>
  </nav>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
nav {
  height: 5rem;
  width: 100%;
  background-color: lightgray;
  display: flex;
  justify-content: flex-end;
  align-items: center;

  h2 {
    text-transform: uppercase;
    margin-right: auto;
  }
}
</style>