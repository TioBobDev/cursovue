<template>
   <div>
    <h1>Olá Vue!</h1>
    <p>Meu nome é {{ nome }}, e minha profissão é {{ profissao }} <br>
    Sou casado com a {{ esposa }}</p>
   </div>
</template>

<script>
    export default {
        name: 'PrimeiroComponente',
        data() {
            return {
                nome: 'Christoffer',
                profissao: 'Programador',
                esposa: 'Ana Paula'
            }
        }
    }
</script>