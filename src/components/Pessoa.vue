<template>
  <div>
    <h2>Esta é a descrição da pessoa {{ nome }}</h2>
    <Info :email="email" :esta_trabalhando="false" />     <!-- esta passando as informações por props-->
    <Form />
  </div>
  
</template>

<script>
import Info from "./Info.vue";
import Form from "./Form.vue";

export default {
  name: "Pessoa",
  components: {
    Info,
    Form,
  },
  data() {
    return {
      nome: "Christoffer",
      email: "christoffer@dev.com.br",
      components: {
        Info,
      },
    };
  },
};
</script>