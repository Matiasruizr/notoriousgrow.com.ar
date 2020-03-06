<template>
    <section class="hero  is-fullheight-with-navbar">
        <div class="hero-body">
            <div class="container">
                <div class="contenedor_texto">
                    <h1>Te estamos rederigiendo a</h1>
                    <h2>Notorious.cl</h2>
                    <h3>En <strong>3</strong> segundos</h3>
                    <b-button type="is-dark"
                        inverted
                        outlined
                        class="cancelar"
                        >
                        Cancelar redirección
                    </b-button>
                    <h4>¿Te gustaria saber más?</h4>
                    <b-button type="is-dark"
                        inverted
                        class="blog"
                        >
                        <span>Visita nuestro blog</span>
                    </b-button>
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
    name: "Hero"
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
            
        }
        h2{
            font-size: 2.5vw;
        }
        h3{
            font-size: 1.5vw;
            margin-bottom: 20px;
            font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif !important;;
            strong{
                color: white;
            }
            
        }
        .cancelar{
            padding: 0 5%;
            margin-bottom: 65px
        }
        h4{
            font-size: 1.5vw;
            margin-bottom: 20px
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

</style>