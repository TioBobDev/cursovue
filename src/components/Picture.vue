<template>
    <img class="size-picture" :src="profile" :alt="descricao">
</template>

<script>

export default {
    name: 'Picture',
    data() {
        return {
            profile: "/img/profile.png",
            descricao: 'Christoffer Raphael Ottebak Pinheiro'
        }
    }
}
</script>