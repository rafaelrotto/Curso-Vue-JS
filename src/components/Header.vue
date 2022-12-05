<template>
    <ul>
        <li><a href="">Teste</a> </li>
        <li><a href="">Teste 2</a> </li>
        <li><a href="">Teste 3</a> </li>
        <li v-if="esta_logado"><a href="#">Meu perfil</a></li>
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
    background: #999;
}

li{
    margin-right: 10px;
}

a{
    color: #ddd;
    text-decoration: none;
    transition: .5s;
}

a:hover {
    color: turquoise; 
}
</style>