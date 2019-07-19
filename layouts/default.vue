<template>
  <div>
    

    <section class="main-content columns">
    <img class="img-desktop-top" src="~/assets/imgtopdesktop.png">
    <img class="img-mobile-top" src="~/assets/imgtopmobile.png">

      <div class="container column is-12">
        <nuxt />
      </div>
    <img class="img-mobile-bottom" src="~/assets/imgbottommobile.png">
    <img class="img-desktop-bottom" src="~/assets/imgbottomdesktop.png">
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
.img-mobile-top,.img-mobile-bottom{
  display: none;
  @media screen and(max-width:426px){
    display:block;
  }
}
.img-desktop-top,.img-desktop-bottom{
  display: block;
  @media screen and(max-width:426px){
    display:none;
  }
}
.img-desktop-top,.img-mobile-top{
  position: absolute;
  top: 0;
  left: 0;
}
.img-desktop-bottom,.img-mobile-bottom{
  position: absolute;
  bottom: -200px;
  left: 0;
}
.img-desktop-bottom{
  bottom: -350px;
}
.img-mobile-bottom{
  bottom: -720px;
  @media screen and(max-width:376px){
    bottom: -600px;
  }
  @media screen and(max-width:321px){
    bottom: -520px;
  }
}
.columns{
  margin-right: 0 !important;
  &:last-child{
    margin-bottom: 0;
  }
}
.main-content{
  height: 930px;
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
.container{
  float: left;
}
</style>

