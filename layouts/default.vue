<template>
  <div class="bg">
    <nav
      class="navbar header has-shadow is-dark"
      role="navigation"
      aria-label="main navigation"
    >
      <div class="navbar-brand">
        <a
          class="navbar-item"
          href="/"
        >
          <img
            src="~/assets/logo-notorious.png"
            alt="Buefy"
            height="28"
          >
        </a>

        
      </div>
    </nav>

    <section class="main-content columns">
      

      <div class="container column is-10">
        <nuxt />
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          title: 'Home',
          icon: 'home',
          to: { name: 'index' }
        },
        {
          title: 'Inspire',
          icon: 'lightbulb',
          to: { name: 'inspire' }
        }
      ]
    }
  }
}
</script>
<style lang="scss" scoped>
.bg{
  background: url(~assets/cannabis.jpg);
  background-size: cover;
  background-attachment: fixed;
  @media screen and(max-width:769px){
     float: left;
  }
}
.columns{
  margin-right: 0 !important;
  &:last-child{
    margin-bottom: 0;
  }
}
.main-content{
  background: rgba(27, 26, 27, 0.7);
  @media screen and(max-width:769px){
    float: left;
  }
}
.navbar-brand{
  margin-left: 50px;
  @media screen and(max-width:769px){
    margin-left: 20px;
  }
  img{
    width: 50px;
    max-height: none;
  }
}
</style>

