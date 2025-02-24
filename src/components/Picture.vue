<template>
    <button @click="mostrarFoto">Mostrar Foto</button>
    <span v-show="verFoto">Foto sendo mostrada</span>
    <img v-show="verFoto" class="size-picture" :src="profile" :alt="descricao">
    
</template>

<script>

export default {
    name: 'Picture',
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
        }
    }
}
</script>