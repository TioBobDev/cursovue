<template>
    <button @click="mostrarFoto">Mostrar Foto</button>
    <span v-show="verFoto">Foto sendo mostrada</span>
    <img v-show="verFoto" class="size-picture" :src="profile" :alt="descricao">
    <MudarImagem @mudar-imagem="trocarImagem"/> <!-- USA O EMIT PARA ENVIAR UM EVENTO PARA O COMPONENTE PAI -->
</template>

<script>

import MudarImagem from './MudarImagem.vue'

export default {
    name: 'Picture',
    components:{
        MudarImagem
    },
    data() {
        return {
            profile: "/img/profile.png",
            descricao: 'Christoffer Raphael Ottebak Pinheiro',
            verFoto: false,
        }
    },
    methods: {
        mostrarFoto(){
            this.verFoto =!this.verFoto;
        },
        trocarImagem(){
            this.profile = "/img/profile2.png"
        }
    }
}
</script>