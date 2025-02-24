<template>
   <div>
    <Reutilizacao />
    <h1>Olá Vue!</h1>
    <p>Meu nome é {{ nome }}, e minha profissão é {{ profissao }} <br>
        <Reutilizacao />
        <Reutilizacao />
    Sou casado com a {{ esposa }}</p>
    <Reutilizacao />
    <Reutilizacao />
    <Reutilizacao />
    <Reutilizacao />
    <Reutilizacao />
    
    <MultiplosEventos/>
   </div>
</template>

<script>
import MultiplosEventos from './MultiplosEventos.vue';
import Reutilizacao from './Reutilizacao.vue';
    export default {
        name: 'PrimeiroComponente',
        components: {
            MultiplosEventos,
            Reutilizacao
        },
        data() {
            return {
                nome: 'Christoffer',
                profissao: 'Programador',
                esposa: 'Ana Paula'
            }
        }
    }
</script>