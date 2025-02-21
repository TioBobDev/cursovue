<template>
  <div>
    <h1>Meu Formulário:</h1>
    <form action="" @submit="enviarFormulario($event)">
   <div>
    <input type="text" v-model="name">
   </div>
    <div>
        <input type="text" v-model="email">
    </div>
    <div>
        <Submit />
    </div>
  </form>
  </div>
</template>

<script>
import InputText from './form/InputText'
import Submit from './form/Submit'

export default {
  name: "Form",
  components: {
    InputText,
    Submit,
  },
  data() {
    return {
      name: 'Christoffer',
      email: 'christoffer@christoffer.com',
    }
  },
  methods: {
    enviarFormulario(e) {
      e.preventDefault();

      const name = this.name;
      const email = this.email;

        console.log('Formulário enviado com sucesso!');
        console.log("O nome é:" + name);
        console.log("O Email é:" + email);

        //Ajax

        //Inserir no banco de dados 
    },
  }
};
</script>