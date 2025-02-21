<template>
    <div>
        <button @click="primeiro(txt1, $event), segundo(txt2, $event), terceiro(txt3, $event), quarto(txt4, $event)">Ativar Multiplos Eventos</button>
        <p>{{ multiplos_eventos }}</p>
    </div>
</template>

<script>
    export default {
      name: 'MultiplosEventos',
      data() {
        return {
          multiplos_eventos: "",
          txt1: "Primeiro evento ativado!",
          txt2: "Segundo evento.",
          txt3: "É, acabou. É só isso mesmo :/",
          txt4: ""
        }
      },
      //conseguimos criar vários métodos e passar vários eventos como demonstrado no botão Ativar Multiplos Eventos
      methods: {
        primeiro(e) {
          this.multiplos_eventos = this.txt1;
        },
        segundo(e) {
            setTimeout(() => this.multiplos_eventos = this.txt2, 1000);
        },
         terceiro(e){
           setTimeout(() => this.multiplos_eventos = this.txt3, 2000);
         },
         quarto(e){
            setTimeout(() => this.multiplos_eventos = this.txt4, 4000);
         }
      }
    }
</script>


<style scoped>

div {
    margin:100px;
}
</style>