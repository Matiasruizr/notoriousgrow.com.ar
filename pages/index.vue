<template>
  <section class="section">
    <!-- <h2 style="color:white">{{country}}</h2> -->
      <Header  />
      <!-- <Hero :country="country"/> -->
      <section class="hero is-fullheight-with-navbar">
        <div class="hero-body contenedor_imagen">
          <div class="container">
            <div class="columns is-centered-mobile">
              <div class="column is-half-desktop">
                <div class="contenedor_texto">
                  <template v-if="country == 'CL' || country == 'ARd'">
                    <h1>Te estamos rederigiendo a</h1>
                    <h2 v-if="country == 'CL'">Notorious.cl</h2>
                    <h2 v-if="country == 'AR'">Notoriousgrow.com.ar</h2>
                    <h3>
                      En
                      <strong>3</strong> segundos
                    </h3>
                    <b-button type="is-dark" inverted outlined class="cancelar" @click="redirect_page = false, country = ''" >Cancelar redirección</b-button>
                  </template>
                  <template v-else>
                    <h1>Bienvenido a NotoriousGrow</h1>
                    <h2>El growshop más grande de Sudamerica</h2>
                  </template>
                  <h4>¿Te gustaria saber más de nosotros?</h4>
                  <a
                    class="button"
                    href="https://notorious.cl/blog/"
                    target="_blank"
                  >Visita nuestro blog</a>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="is-block has-text-centered">
          <div class="cursor" @click="scrollDown()">
            <b-icon class="icono" :icon="toggleIcon" size="is-small"></b-icon>
          </div>
          <p>Si no se te redirecciona automáticamente, por favor haz click en la bandera que corresponda</p>
        </div>
      </section>

      <Paises />
      <Footer />
  </section>
</template>


<script>
import Header from '~/components/Header'
import Paises from '~/components/Paises'
import Footer from '~/components/Footer'

import axios from 'axios'

export default {
  name: 'HomePage',
  data () {
    return{
      country: '',
      redirect_page: true,
      togglePosition: false,
      toggleIcon: "chevron-down",
      redirect_location: ''
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
            self.redirect_location = 'https://notorious.cl/'
          } else if (self.country == 'AR') {
            console.log(self.country)
            self.redirect_location = 'http://notoriousgrow.com.ar/'
          } else {
            console.log('ninguno');
          }
          setTimeout(function(){ 
            if (self.redirect_page == true) {
              if (process.browser) {
                window.location.replace(self.redirect_location)
              }
            }
          }, 3000)
        })
        .catch(function(error){
          console.log(error)
        })
  },
  components: {
    Header,
    Paises,
    Footer
  },
  methods: {
    scrollDown() {
      this.togglePosition = !this.togglePosition;
      let div;
      if (this.togglePosition == true) {
        div = ".banderas";
        this.toggleIcon = "chevron-up";
      } else {
        div = ".hero";
        this.toggleIcon = "chevron-down";
      }
      let element = document.querySelector(div);
      element.scrollIntoView({ behavior: "smooth", block: "end" });
    }
  }
}
</script>

<style lang="scss" scoped>
.cursor:hover {
  cursor: pointer;
}
.contenedor_texto {
  @media (max-width: 767px) {
    text-align: center;
  }
  margin-top: -5%;
  h1 {
    font-size: 2.9vw;
    @media (max-width: 768px) {
      font-size: 17px;
      margin-bottom: 15px;
    }
  }
  h2 {
    font-size: 2.5vw;
    @media (max-width: 768px) {
      font-size: 14px;
      margin-bottom: 15px;
    }
  }
  h3 {
    font-size: 1.5vw;
    margin-bottom: 20px;
    font-family: "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
      "Lucida Sans Unicode", Geneva, Verdana, sans-serif !important;
    strong {
      color: white;
    }
    @media (max-width: 768px) {
      font-size: 13px;
    }
  }
  .cancelar {
    padding: 0 5%;
    margin-bottom: 65px;
  }
  h4 {
    font-size: 1.5vw;
    margin-bottom: 20px;
    @media (max-width: 768px) {
      font-size: 13px;
    }
  }
  .blog {
    font-size: 1vw;
    padding: 3% 5%;
    font-weight: 800;
  }
}
.contenedor_imagen {
  background-image: url("../assets/img/mari.png");
  background-position: bottom;
  background-size: 75%;
  background-repeat: no-repeat;
  @media (min-width: 768px) {
    background-size: 50%;
    background-position: right center;
  }
}
.icono {
  $size: 12vw;
  color: black;
  background-color: white;
  font-size: $size;
  height: $size;
  width: $size;
  border-radius: 50%;
  @media (min-width: 545px) {
    font-size: calc(#{$size} / 3);
    height: calc(#{$size} / 3);
    width: calc(#{$size} / 3);
  }
}
p {
  margin-top: 5%;
  @media (min-width: 768px) {
    font-size: 1.5vw;
  }
}
.hero-body {
  @media (max-width: 768px) {
    display: block !important;
  }
}
.hero.is-fullheight-with-navbar {
  @media (max-width: 768px) {
    min-height: auto;
  }
}
</style>