<template>
  <div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>
      Não estou trabalhando no momento. Procurando novas oportunidades
    </p>
    <p>Utilizo as seguintes tecnologias.</p>
    <ul>
      <li v-show="programo_PHP">PHP</li>
      <li v-show="programo_vue">Vue</li>
      <li v-show="programo_phyton">Python</li>
      <li v-show="programo_java">Java</li>
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
      programo_PHP: true,
      programo_java: false,
      programo_vue: true,
      programo_phyton: true,
      mostrar_email: false,
      email: "meuemail@meuemail.com",
      meu_link: "https://github.com/TioBobDev",
      textoBotao: "Mostra e-mail",
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