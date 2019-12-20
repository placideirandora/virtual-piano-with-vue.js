<template>
  <div class="app">
    <img alt="Piano Logo" src="./assets/icons/keyboard.svg" class="app__logo">
    <h1 class="app__title">Virtual Piano</h1>
  </div>
</template>

<script>
export default {
  name: 'app',
}
</script>

<style lang="scss">
body {
  background:  #E9F0F2;
}

.app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;

  &__logo {
    width: 8rem;
  }

  &__title {
    font-size: 3rem;
    text-transform: uppercase;
  }
}
</style>
