<template>
    <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Sobre</a></li>
        <li><a href="#">Contato</a></li>
        <li v-if="esta_logado"><a href="#">Meu Perfil</a></li>
    </ul>
</template>

<script>
export default{
    name: 'Header',
    props: ["esta_logado"]
}
</script>

<style scoped>
    ul{
        list-style: none;
        display: flex;
        background-color: rgb(63, 59, 53);
    }

    li{
        margin-right: 20px;
    }

    a{
        text-decoration: none;
        color:antiquewhite;
        transition: .5s;
    }
    
    a:hover{
        color:rgb(22, 190, 241);
    }
</style>