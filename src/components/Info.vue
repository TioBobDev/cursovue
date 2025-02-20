<template>
  <div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>
      Não estou trabalhando no momento. Procurando novas oportunidades
    </p>
    <p>Utilizo as seguintes tecnologias para back-end:</p>
    <ul>
      <!-- AQUI EU PASSO DENTRO DO V-FOR O ARGUMENTO QUE EU QUERO RENDERIZAR NO LAÇO E DEPOIS A CHAVE, NESTE CASO INDEX, ATRIBUIDA PELO v-bind:key -->
      <li v-for="(backend, index) in programoBackend" v-bind:key="index">
        {{ backend }}
      </li>
    </ul>
    <p>Utilizo as seguintes tecnologias para front-end:</p>
    <ul>
      <li v-for="frontend in programoFrontend" :key="frontend.id">
        {{ frontend.language }}
      </li>
    </ul>
    <div>
      <button @click="ShowEmail">{{ textoBotao }}</button>
    </div>
    <p v-show="mostrar_email">
      Gostou do meu currículo? Mande um email para: {{ email }}
    </p>
    <!-- o v-bind,ou apenas :, permite que eu consiga acessar o link dinamicamente -->
    <p>
      Para acessar meu portifólio,
      <a v-bind:href="meu_link" target="_blank">basta clicar aqui</a>
    </p>
    <div>
      <Picture />
    </div>
  </div>
</template>

<script>
import Picture from "./Picture.vue"; // importando o componente Picture.vue

export default {
  name: "Info",
  components: {
    Picture,
  },
  data() {
    return {
      esta_trabalhando: false,
      mostrar_email: false,
      email: "meuemail@meuemail.com",
      meu_link: "https://github.com/TioBobDev",
      textoBotao: "Mostra e-mail",
      programoBackend: ["PHP", "Java", "Python"],
      programoFrontend: [
        { id: 1, language: "HTML" },
        { id: 2, language: "CSS" },
        { id: 3, language: "Vue.js" },
        { id: 4, language: "Node.js" },
      ],
    };
  },
  methods: {
    ShowEmail() {
      this.mostrar_email = !this.mostrar_email;
      if (!this.mostrar_email) {
        this.textoBotao = "Mostrar e-mail";
      } else {
        this.textoBotao = "Ocultar e-mail";
      }
    },
  },
};
</script>