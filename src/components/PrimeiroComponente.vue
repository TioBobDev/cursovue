<template>
   <div>
    <h1>Olá Vue!</h1>
    <p>Meu nome é {{ nome }}, e minha profissão é {{ profissao }} <br>
    Sou casado com a {{ esposa }}</p>
    
    <MultiplosEventos/>
   </div>
</template>

<script>
import MultiplosEventos from './MultiplosEventos.vue';
    export default {
        name: 'PrimeiroComponente',
        components: {
            MultiplosEventos,
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