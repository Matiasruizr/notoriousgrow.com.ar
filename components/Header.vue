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
<style lang="scss" scoped>
    .contenedor{
        display: flex;
        justify-content: center

    }
    h1{
        text-align: center;
        font-size: 3vw;
        @media(max-width: 768px) {
            margin-top: 5px;
            font-size: 18px;
        }
    }
    img{
        width: 5vw;
        height: 5vw;
        margin-right: 32px;
        @media(max-width: 768px) {
            width: 45px;
            height: 45px;
        }
    }
</style>