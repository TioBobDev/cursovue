<template>
  <div>
    <h1>Meu Formulário:</h1>
    <form action="">
   <div>
    <InputText />
   </div>
    <div>
        <InputText />
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
};
</script>