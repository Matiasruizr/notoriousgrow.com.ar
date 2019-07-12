<template>
  <section class="section">
    <div class=" logo column is-12">
      <img src="~/assets/logo-notorious.png">
    </div>
      <div class="btn column is-6">
        <a href="https://notorious.cl/"><h1>Notorious Chile</h1>
        <img src="~/assets/chile.png"></a>
      </div>
      <div class="btn column is-6">
        <a href="http://notoriousgrow.com.ar/"><h1>Notorious Argentina</h1>
        <img src="~/assets/argentina.png"></a>
      </div>
  </section>
</template>

<script>
import Card from '~/components/Card'

export default {
  name: 'HomePage',

  components: {
    Card
  }
}
</script>
<style lang="scss" scoped>
.logo{
  width: 100%;
  float: left;
  img{
    width: 15%;
    display: block;
    margin: 0 auto;
    @media screen and(max-width:426px){
      width: 30%;
    }
  }
}
.btn{
  
  margin: 60px 0 110px 0;
  float: left;
  @media screen and(max-width:769px){
    width: 50%;
    margin-bottom: 130px;
  }
  @media screen and(max-width:426px){
    width: 100%;
    margin: 18px 0;
  }
  @media screen and(max-width:376px){
    margin: 28px 0;
  }
  @media screen and(max-width:321px){
    margin: 30px 0;
  }
  h1{
    font-weight: bold;
    color: #ffffff;
    float: left;
    margin-bottom: 30px;
    font-size: 32px;
    width: 100%;
    text-align: center;
    transition: 200ms;
    &:hover{
      color: #7e005a;
    }
    @media screen and(max-width:426px){
      font-size:25px;
    }
  }
  img{
    display: block;
    margin: 0 auto;
    width: 40%;
    transition: 200ms;
    &:hover{
      transform: scale(1.1);
    }
  }
}
</style>

