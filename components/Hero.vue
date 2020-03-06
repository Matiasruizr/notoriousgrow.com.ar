<template>
    <section class="hero  is-fullheight-with-navbar" >
        <div class="hero-body">
            <div class="container">
                <div class="contenedor_texto">
                    <template v-if="country == 'CL' || country == 'ARd'">
                        <h1>Te estamos rederigiendo a</h1>
                        <h2 v-if="country == 'CL'">Notorious.cl</h2>
                        <h2 v-if="country == 'AR'">Notoriousgrow.com.ar</h2>
                        <h3>En <strong>3</strong> segundos</h3>
                        <b-button type="is-dark"
                            inverted
                            outlined
                            class="cancelar"
                            >
                            Cancelar redirección
                        </b-button>
                    </template>
                    <template v-else>
                        <h1>Bienvenido a NotoriousGrow</h1>
                        <h2>El growshop más grande de Sudamerica</h2>
                      
                    </template>
                    <h4>¿Te gustaria saber más de nosotros?</h4>
                    <a class="button" href="https://notorious.cl/blog/" target="_blank" >
                        Visita nuestro blog 
                    </a>
           
                </div>
                <div class="contenedor_imagen">
                    
                </div>
                
            </div>
            
        </div>
        <div class="is-block has-text-centered">
                <div >
                    <b-icon
                        class="icono"
                        icon="chevron-down"
                        size="is-small">
                    </b-icon>
                </div>
                <p>Si no se te redirecciona automáticamente, por favor haz click en la bandera que corresponda</p>
            </div>
    </section>
</template>
<script>
export default {
    name: "Hero",
    props: ['country']
}
</script>
<style lang="scss" scoped>
    .container{
        display: grid;
        grid-template-columns: repeat(2,1fr);
        margin-top: -5vw
    }
    .contenedor_texto{
        width: 40vw;
        padding: 10vw 0;
        margin-top: -5%;
        h1{
            font-size: 2.9vw;
            @media(max-width: 768px) {
                font-size: 17px;
                margin-bottom: 15px;
            }
        }
        h2{
            font-size: 2.5vw;
            @media(max-width: 768px) {
                font-size: 14px;
                margin-bottom: 15px;
            }
        }
        h3{
            font-size: 1.5vw;
            margin-bottom: 20px;
            font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif !important;;
            strong{
                color: white;
            }
            @media(max-width: 768px) {
                font-size: 13px;
            }
            
        }
        .cancelar{
            padding: 0 5%;
            margin-bottom: 65px
        }
        h4{
            font-size: 1.5vw;
            margin-bottom: 20px;
            @media(max-width: 768px) {
                font-size: 13px;
            }
        }
        .blog{
            font-size: 1vw;
            padding: 3% 5%;
            font-weight: 800
        }
    }
    .contenedor_imagen{
        background-image: url('../assets/img/mari.png');
        background-size: cover;
        background-position: center top;

    }
    .icono{
        font-size: 4vw;
        color:black;
        background-color: white;
        width: 4vw;
        height: 4vw;
        border-radius: 50%;
        position: absolute;
        margin-top: -180px
    }
    p{
        font-size: 1.5vw;
        margin-top: 5%
    }
   .hero-body{
       @media(max-width: 768px) {
          display: block!important; 
       }
   }
   .hero.is-fullheight-with-navbar {
        @media(max-width: 768px) {
            min-height: auto;
        }
   }
</style>