<template>
  <section class="fotos has-text-centered">
    <p class="my-3">Siguenos en instagram</p>
    <div class="container">
      <div class="columns is-centered is-multiline is-mobile">
        <div class="column is-half-mobile">
          <a href="https://www.instagram.com/p/B9U-x7gg5si/" target="_blank">
            <img src="../assets/img/1.png" alt="1" />
          </a>
        </div>
        <div class="column is-half-mobile">
          <a href="https://www.instagram.com/p/B9P0gKfg1d2/" target="_blank">
            <img src="../assets/img/2.png" alt="1" />
          </a>
        </div>
        <div class="column is-half-mobile">
          <a href="https://www.instagram.com/p/B9IIa-uAK1e/" target="_blank">
            <img src="../assets/img/3.png" alt="1" />
          </a>
        </div>
        <div class="column is-half-mobile">
          <a href="https://www.instagram.com/p/B9C9F8Cgqz-/" target="_blank">
            <img src="../assets/img/4.png" alt="1" />
          </a>
        </div>
        <div class="column is-half-mobile">
          <a href="https://www.instagram.com/p/B8-C1J_gqho/" target="_blank">
            <img src="../assets/img/5.png" alt="1" />
          </a>
        </div>
      </div>
    </div>
    <div class="container">
      <div class="columns is-centered">
        <div class="column">
          <p class="foot">
            Sitio diseñado y desarrollado por
            <strong
              class="has-text-white"
            >Notorious - El growshop más grande de Sudamerica</strong>
          </p>
          <img class="logo" src="../assets/img/logo.png" alt="logo" />
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: "Footer"
}
</script>
<style lang="scss" scoped>
.my-3 {
      margin: 1.3em 0;
}
.foot {
  @media (min-width: 767px) {
    font-size: 0.8vw;
  }
  font-family: "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
    "Lucida Sans Unicode", Geneva, Verdana, sans-serif !important;
}
.logo {
  width: 100px;
  margin: 2% 0;
  @media (min-width: 767px) {
    width: 5vw;
  }
}
</style>