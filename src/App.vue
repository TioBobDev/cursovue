<template>
    <div>
      <Header :esta_logado="true" />    <!-- esta passando as informações por props no modo array-->
      <PrimeiroComponente />
      <p>{{ nome }}</p>
      <LifeCycle />
      <Pessoa />
    </div>

</template>

<script>
import Header from './components/Header.vue'
import PrimeiroComponente from './components/PrimeiroComponente.vue'
import LifeCycle from './components/LifeCycle.vue'
import Pessoa from './components/Pessoa.vue'
  
export default {
    name: 'App',
    components: {
      PrimeiroComponente,
      LifeCycle,
      Pessoa,
      Header, 
    }, 
    data() {
      return {
        nome: 'John Doe'
      }
    }

  }
</script>

<style>

    body {
      background-color: rgb(33, 37, 26);
      color: white;
    }

    a{
      color: red;
    }
   
    .teste{
      color: blue;
      background-color: #fff;
    }

</style>