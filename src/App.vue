<template>
    <div>
      <PrimeiroComponente />
      <p>{{ nome }}</p>
      <LifeCycle />
    </div>

</template>

<script>
import LifeCycleVue from './components/LifeCycle.vue'

import PrimeiroComponente from './components/PrimeiroComponente.vue'
import LifeCycle from './components/LifeCycle.vue'
  
export default {
    name: 'App',
    components: {
      PrimeiroComponente,
      LifeCycle,
    }, 
    data() {
      return {
        nome: 'John Doe'
      }
    }

  }
</script>