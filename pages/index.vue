<template>
  <section class="section">
      <Header />
      <Hero />
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
  date(){
    return{
      country: ''
    }
  },

  components: {
    Header,
    Hero,
    Paises,
    Footer
  },
  mounted(){
    // let self = this
    // axios.get(`https://ipapi.co/json/`,{
    //   headers: {
    //     'Content-Type': 'aplication/json',
    //   }
    // })
    // .then(function(response) {
    //   console.log(response.data.country);
    //   self.country=response.data.country;
    //   if (self.country == 'CL'){
    //     console.log(self.country)
    //     location.replace('https://notorious.cl/')
    //   };
    //   if (self.country == 'AR') {
    //     console.log(self.country)
    //     location.replace('http://notoriousgrow.com.ar/')
    //   }
    // })
    // .catch(function(error){
    //       console.log(error)
    // })
  }
}
</script>
