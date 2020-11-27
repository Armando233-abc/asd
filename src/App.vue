<template>
  <div id="app">
    <AppFooter />
  </div>
</template>

<script>
import AppFooter from './components/AppFooter'
export default {
  name: 'App',
  components: {
    AppFooter
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100vh;
}

body{
  --verde: #59886b;
  --rosso: #c05555;
  --panna: #fff8c1;
  --bianco: #ffffff; 
  background-color: var(--verde);
  margin: 0;
  padding: 0;
  height: 100vh;
}
</style>
