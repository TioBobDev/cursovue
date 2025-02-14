<template>
    <div>
      <PrimeiroComponente />
      <p>{{ nome }}</p>
    </div>

</template>

<script>

import PrimeiroComponente from './components/PrimeiroComponente.vue'
  
export default {
    name: 'App',
    components: {
      PrimeiroComponente
    }, 
    data() {
      return {
        nome: 'John Doe'
      }
    }

  }
</script>