<template>
  <div>
    <Header />
    <PrimeiroComponente/>
    <h4>O dado do app é: {{ testando }}</h4>
    <life-cycle />
    <pessoa />
  </div>
</template>

<script>
  import PrimeiroComponente from './components/PrimeiroComponente'
  import lifeCycle from './components/lifeCycle'
  import pessoa from './components/pessoa'
  import Header from './components/Header.vue'

  export default {
    name: 'App',
    components: {
      PrimeiroComponente,
      lifeCycle,
      pessoa,
      Header
    },

    data() {
      return {
        testando: 'Teste'
      }
    }
  }
</script>

<style>
/* *{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
} */
body{
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  background: rgb(97, 97, 97);
  color: #fff;
}
a{
  color: rgb(255, 41, 41);
}
.teste{
  background: black;
}
</style>