<template>
    <div class="container has-text-centered  ">
        <div class="contenedor">
            <img src="../assets/img/logo.png" alt="logo">
        <h1 class="has-text-centered">GROWSHOP ONLINE</h1>
        </div>
    </div>
</template>
<script>
export default {
    name:'Header'
}
</script>
<style lang="css" scoped>
    .contenedor{
        display: flex;
        justify-content: center

    }
    h1{
        text-align: center;
        font-size: 3vw;
    }
    img{
        width: 5vw;
        height: 5vw;
        margin-right: 32px;
    }
</style>