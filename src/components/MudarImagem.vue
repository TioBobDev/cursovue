<template>
    <div>
        <button @click="$emit('mudarImagem')">TROCAR IMAGEM DE PERFIL</button>
    </div>
</template>

<script>
    export default {
        name:'MudarImagem',
        emits: ['mudarImagem']
    }
</script>