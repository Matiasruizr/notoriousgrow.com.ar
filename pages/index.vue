<template>
  <section class="section">
    <!-- <h2 style="color:white">{{country}}</h2> -->
      <Header  />
      <Hero :country="country"/>
      <Paises />
      <Footer />
  </section>
</template>


<script>
import Header from '~/components/Header'
import Hero from '~/components/Hero'
import Paises from '~/components/Paises'
import Footer from '~/components/Footer'

import axios from 'axios'

export default {
  name: 'HomePage',
  date() {
    return{
      country: ''
    }
  },


  created(){
 
    let self = this;
    axios.get(`https://ipapi.co/json/`,{
      headers: {
        'Content-Type': 'aplication/json',
      }
    })
    .then(function(response) {

      self.country= response.data.country;
      if (self.country == 'CL'){
        console.log(self.country)
        // location.replace('https://notorious.cl/')
      } else if (self.country == 'AR') {
        console.log(self.country)
        // location.replace('http://notoriousgrow.com.ar/')
      } else {
        console.log('ninguno');
      }
    })
    .catch(function(error){
        console.log(error)
    })
  },
  components: {
    Header,
    Hero,
    Paises,
    Footer
  },
}
</script>
