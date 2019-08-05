<template>
  <section class="section">
    
    <div class=" logo column is-12">
      <img class="logo-img" src="~/assets/logo-notorious.png">
      <img src="~/assets/growshoponline.png">
    </div>
      <div class="btn column is-6">
        <a href="https://notorious.cl/"><h1>Chile</h1>
        <img src="~/assets/chile.png"></a>
        <hr>
        <a href="http://notoriousgrow.com.ar/"><h1>Argentina</h1>
        <img src="~/assets/argentina.png"></a>
      </div>
      <div class="frase column is-6">
        <img src="~/assets/frase.png">
        <a href="http://notorious.cl/blog/">Notorious Blog</a>
      </div>
    
  </section>
</template>
<script>
import Card from '~/components/Card'
import axios from 'axios'

export default {
  name: 'HomePage',
  date(){
    return{
      country: ''
    }
  },

  components: {
    Card
  },
  mounted(){
    let self = this
    axios.get(`https://ipapi.co/json/`,{
      headers: {
        'Content-Type': 'aplication/json',
      }
    })
    .then(function(response) {
      console.log(response.data.country);
      self.country=response.data.country;
      if (self.country == 'CL'){
        console.log(self.country)
        location.replace('https://notorious.cl/')
      };
      if (self.country == 'AR') {
        console.log(self.country)
        location.replace('http://notoriousgrow.com.ar/')
      }
    })
    .catch(function(error){
          console.log(error)
    })
  }
}
</script>
<style lang="scss" scoped>
.section{
  float: left;
  width: 100%;
}

.logo{
  width: 100%;
  float: left;
  img{
    width: 70%;
    margin: 0 auto;
    display: block;
    margin-top: 35px;
    @media screen and(max-width: 426px){
      width: 100%;
    }
  }
  .logo-img{
    width: 15%;
    float: left;
    margin: 0;
    @media screen and(max-width:426px){
    display: block;
    margin: 0 auto;
    float: none;
      width: 30%;
    }
  }
}
.frase{
  float: left;
  margin: 170px 0 110px 0;
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
  img{
    float: initial;
  }
  a{
    margin: 0 auto;
    margin-left: 33%;
    margin-top: 40px;
    font-size: 20px;
    float: left;
    padding: 10px 30px;
    border: solid 1px #fff;
    font-weight: bold;
    border-radius: 5px;
    color: #ffffff;
    background: #7e005a;
    transition: 300ms;
    @media screen and(max-width:1025px){
    margin-left: 27%;
  }
     @media screen and(max-width:769px){
    margin-left: 20%;
  }
    @media screen and(max-width:426px){
     font-size: 16px;
     margin-left: 27%;
     padding: 5px 15px; 
    }
    @media screen and(max-width:321px){
    margin-left: 19%;
  }
    &:hover{
      border-color: #7e005a;
      background: #fff;
      color: #7e005a;
    }

  }
}
.btn{
  
  margin: 170px 0 110px 0;
  float: left;
  @media screen and(max-width:769px){
    width: 50%;
    margin-bottom: 130px;
  }
  @media screen and(max-width:426px){
    width: 100%;
    margin: 18px 0;
    margin-top: 120px;
  }
  @media screen and(max-width:376px){
    margin: 28px 0;
    margin-top: 120px;
  }
  @media screen and(max-width:321px){
    margin: 30px 0;
    margin-top: 120px;
  }
  hr{
    background-color: #000;
  }
  h1{
    color: #000;
    float: left;
    font-family: 'PunkRocker';
    margin-bottom: 30px;
    font-size: 70px;
    width: 40%;
    text-align: center;
    transition: 200ms;
    &:hover{
      color: #7e005a;
    }
    @media screen and(max-width:426px){
      font-size:70px;
      width: 100%;
    }
  }
  img{
    display: block;
    margin: 0 auto;
    width: 40%;
    transition: 200ms;
    @media screen and(max-width:426px){
      width: 70%;
    }
    &:hover{
      transform: scale(1.1);
      -webkit-box-shadow: 0px 0px 38px -13px rgba(0,0,0,0.75);
-moz-box-shadow: 0px 0px 38px -13px rgba(0,0,0,0.75);
box-shadow: 0px 0px 38px -13px rgba(0,0,0,0.75);
    }
  }
}
</style>

