<template>
  <HeaderComponente/>
  <PrimeiroComponente/>
  <LifeCycle/>
  <PessoaComponente/>
</template>

<script>
  //imports dos componentes
  import PrimeiroComponente from './components/PrimeiroComponente.vue'
  import LifeCycle from './components/LifeCycle.vue'
  import PessoaComponente from './components/PessoaComponente.vue'
  import HeaderComponente from './components/HeaderComponente.vue';

  export default{
    name : "App",

    components : {
    PrimeiroComponente,
    LifeCycle,
    PessoaComponente,
    HeaderComponente
}
  }
</script>

<style>
  body {
    background-color: #333;
    color: #fff;
  }

  a {
    color: red;
  }

  .teste {
    background-color: black;
  }

</style>