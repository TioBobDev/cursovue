<template>
    <div>
      <PrimeiroComponente />
      <p>{{ nome }}</p>
      <LifeCycle />
      <Pessoa />
    </div>

</template>

<script>
import LifeCycleVue from './components/LifeCycle.vue'

import PrimeiroComponente from './components/PrimeiroComponente.vue'
import LifeCycle from './components/LifeCycle.vue'
import Pessoa from './components/Pessoa.vue'
  
export default {
    name: 'App',
    components: {
      PrimeiroComponente,
      LifeCycle,
      Pessoa, 
    }, 
    data() {
      return {
        nome: 'John Doe'
      }
    }

  }
</script>