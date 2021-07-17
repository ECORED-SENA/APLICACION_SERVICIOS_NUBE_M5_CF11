<template lang="pug">
.curso-main-container.introduccion
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal
      .titulo-principal__numero
        span 2
      h1 Sistema de control de versiones - Git

    p(data-aos="fade-up") Git es un sistema de control de versiones que nació en el año 2005 producto de las necesidades que afrontaba la comunidad del kernel de Linux de encontrar un mecanismo que les permitiera soportar las actualizaciones y mantenimientos que requería este gran proyecto. Según Git (2021), algunos de los objetivos trazados que debía cumplir este nuevo mecanismo incluían:

    .bloque-texto-a.color-secundario.p-4.p-md-5.mt-5(data-aos="fade-up")
      .row.m-0.align-items-center.justify-content-between
        .col-lg-4.mb-4.mb-lg-0
          figure.p-5.bg-white(style="border-radius:10px;")
            img.imagen_flotante_animada(src="@/assets/curso/tema2/1.svg")
        .col-lg-8
          .bloque-texto-a__texto.p-4
            ol.lista-ol--cuadro.lista-ol--separador
              li(data-aos="fade-up")
                .lista-ol--cuadro__vineta
                  span a
                | Velocidad.
              li(data-aos="fade-up")
                .lista-ol--cuadro__vineta
                  span b
                | Diseño sencillo.
              li(data-aos="fade-up")
                .lista-ol--cuadro__vineta
                  span c
                | Soporte para múltiples desarrollos no lineales.
              li(data-aos="fade-up")
                .lista-ol--cuadro__vineta
                  span d
                | Debía ser un sistema totalmente distribuido. 
              li(data-aos="fade-up")
                .lista-ol--cuadro__vineta
                  span e
                | Debía ser capaz de manejar eficientemente proyectos de gran envergadura.

    p.mt-5(data-aos="fade-up") Git, a diferencia de otros sistemas de control de versiones, posee un sistema de almacenamiento de información en los que cada versión posee una copia de instantáneas en miniatura, es decir, ofrece la posibilidad de trabajo aun cuando no se tiene conectividad al servidor central, ya que localmente se posee toda la información requerida incluso si se desea hacer procesos de recuperación a versiones anteriores.

    p.mt-3(data-aos="fade-up") Git hace un proceso de comprobación antes de realizar el almacenamiento de datos mediante unos procesos algorítmicos con códigos criptográficos SHA-1, que son calculados a partir del contenido y estructura de directorio del proyecto, lo cual hace imposible cambiar el contenido de algún archivo o de la estructura de directorios sin que Git lo detecte.

    p.mt-3(data-aos="fade-up") Debido a que Git solo añade información a la base de datos con cualquier acción realizada, es difícil llegar a un estado en el que este sistema control de versiones no pueda hacer un proceso de recuperación o que se elimine información de alguna manera una vez exista una confirmación en los cambios.

    .row.mt-5
      .col-md-4.mb-3
        .bloque-texto-c.color-secundario.p-4(data-aos="fade-right" style="height:100%;")
          i.fas.fa-quote-right
          h3.mb-5.mt-4 Según Git (2021), el sistema de control de versiones Git maneja tres estados principales para cada uno de los archivos de un proyecto, los cuales son:

          span.mt-5 Git (2021)
      .col-md-8
        .row.mb-3.mt-5
          .col-md-4.mb-3.text-center(data-aos="fade-up")
            span.item_round.image_floating.show_texto_1(style="background-color:#FFCA28;") 1

            p.mt-4 #[strong Confirmado (committed)]

          .col-md-4.mb-3.text-center(data-aos="fade-up")
            span.item_round.image_floating.show_texto_2(style="background-color:#4DD0E1;") 2

            p.mt-4 #[strong Preparado (staged)]

          .col-md-4.mb-3.text-center(data-aos="fade-up")
            span.item_round.image_floating.show_texto_3(style="background-color:#4DD0E1;") 3

            p.mt-4 #[strong Modificado (modified)]

        .p-5(style="background-color:#E0FBFF;" data-aos="fade-up")
          p.texto_1.texto_show Indica que los datos se encuentran almacenados de forma segura en la base de datos local. Se considera una versión concreta.
          p.texto_2.texto_show(style="display:none") Indica un archivo modificado que ha sido marcado en su versión actual para una próxima confirmación.
          p.texto_3.texto_show(style="display:none") Indica un que el archivo ha sufrido alguna modificación, pero esta aún no se ha preparado ni confirmado en la base de datos.

    p.mt-4(data-aos="fade-up") En la siguiente figura se puede observar la interacción que ocurre entre el directorio de trabajo que es donde se desarrolla las labores de construcción del proyecto y corresponde a una copia de la versión del proyecto, el área de preparación es un archivo que almacena información de lo que va en la próxima confirmación y el directorio Git es donde se almacenan los metadatos y base de datos de objetos para el proyecto. Este directorio Git es lo que se copia en el proceso de clonación del repositorio desde otro equipo de trabajo.

    br
    p.mt-5(style="border-left:4px #4DD0E1 solid;padding-left:8px;" data-aos="fade-right") #[strong Figura 1] Flujo de archivos de acuerdo con el estado

    .col-md-9.m-auto
      figure.mt-5.image_floating
        img(src="@/assets/curso/tema2/2.svg")
        figcaption Nota. Tomada de Git (2021)

    p.mt-5(data-aos="fade-up") Teniendo en cuenta lo anterior, un flujo normal de acciones para trabajar con Git sería el siguiente:

    .bloque-texto-a.color-secundario.p-4.p-md-5.mt-5(data-aos="fade-up")
      .row.m-0.align-items-center.justify-content-between
        .col-lg-4.mb-4.mb-lg-0
          figure.p-5.bg-white(style="border-radius:10px;")
            img.imagen_flotante_animada(src="@/assets/curso/tema2/1.svg")
        .col-lg-8
          .bloque-texto-a__texto.p-4
            ol.lista-ol--cuadro.lista-ol--separador
              li(data-aos="fade-up")
                .lista-ol--cuadro__vineta
                  span a
                | Realizar acciones de construcción del proyecto sobre el directorio de trabajo.
              li(data-aos="fade-up")
                .lista-ol--cuadro__vineta
                  span b
                | Realizar la preparación de los archivos, los cuales se marcaron para ser añadidos al área de preparación.
              li(data-aos="fade-up")
                .lista-ol--cuadro__vineta
                  span c
                | Confirmar los cambios, lo cual toma los archivos del área de preparación y los almacena como una copia instantánea permanente en el directorio Git.

    .cajon.color-acento-botones.p-4.mt-5.caja_escalada_hover.row.fade-in-image.caja_flotante_rosada(data-aos="fade-up")
      p Git se puede instalar en cualquier tipo y distribución de sistema operativo e incluso se puede integrar con diferentes IDE para conexión con varios repositorios locales y en la nube. Para un mejor entendimiento de los comandos más comúnmente utilizados se optará por la instalación común y manipulación de este por consola de comandos.

    br
    br
    .titulo-segundo#t_2_1.mt-5
      h2 2.1 Instalación de Git en sistemas operativos Windows

    p(data-aos="fade-up") La forma más sencilla de instalar Git en sistemas operativos Windows es por medio del sitio oficial disponible, el cual se podrá encontrar en el material complementario del componente.

    .tarjeta.text-white.p-5.mt-5.caja_flotante_azul(data-aos="fade-up" style="background: linear-gradient(#0f3664,rgb(57 131 199));")
      .row.justify-content-around.align-items-center
        .col-4.col-sm-2.col-lg-2
          img.imagen_flotante_animada(src="@/assets/curso/tema2/3.svg")
        .col
          .row.justify-content-between.align-items-center
            .col.mb-3.mb-sm-0
              .h4.mb-0 Instalación de git en sistemas operativos Windows
              p.mt-2 A continuación, se describe el paso a paso del proceso de instalación para este sistema.
            .col-sm-auto
              a.boton.boton--b.color-acento-secundario(:href="obtenerLink('downloads/CF11_2_1_Instalacion_Git_Sistemas_Operativos_Windows.docx')" target="_blank")
                span(style="color: #12263F !important;") Descargar
                i.fas.fa-file-download(style="color: #12263F !important;")

    br
    br
    .titulo-segundo#t_2_2.mt-5
      h2 2.2 Instalación de Git distribuciones de Linux

    p(data-aos="fade-up") En el caso del sistema operativo Linux se puede hacer por medio de la herramienta de administración de paquetes. A continuación, podrá conocer sobre este proceso de instalación:

    .tarjeta.text-white.p-5.mt-5.caja_flotante_azul(data-aos="fade-up" style="background: linear-gradient(#0f3664,rgb(57 131 199));")
      .row.justify-content-around.align-items-center
        .col-4.col-sm-2.col-lg-2
          img.imagen_flotante_animada(src="@/assets/curso/tema2/3.svg")
        .col
          .row.justify-content-between.align-items-center
            .col.mb-3.mb-sm-0
              .h4.mb-0 Instalación de Git distribuciones de Linux
              p.mt-2 A continuación, se describe el paso a paso del proceso de instalación para este sistema.
            .col-sm-auto
              a.boton.boton--b.color-acento-secundario(:href="obtenerLink('downloads/CF11_2_2_Instalacion_Git_Distribuciones_Linux.docx')" target="_blank")
                span(style="color: #12263F !important;") Descargar
                i.fas.fa-file-download(style="color: #12263F !important;")

</template>
<script>
import $ from 'jquery'
export default {
  name: 'Tema2',
  data: () => ({
    mostrarIndicador: true,
    modal1: false,
  }),
  mounted() {
    this.$nextTick(() => {
      this.$aosRefresh()
    })
    $('.show_texto_1').click(function() {
      $('.texto_2').hide()
      $('.texto_3').hide()
      $('.texto_1').show()
      $(this).css('background-color', '#FFCA28')
      $('.show_texto_2').css('background-color', '#4DD0E1')
      $('.show_texto_3').css('background-color', '#4DD0E1')
    }),
      $('.show_texto_2').click(function() {
        $('.texto_1').hide()
        $('.texto_3').hide()
        $('.texto_2').show()
        $(this).css('background-color', '#FFCA28')
        $('.show_texto_1').css('background-color', '#4DD0E1')
        $('.show_texto_3').css('background-color', '#4DD0E1')
      }),
      $('.show_texto_3').click(function() {
        $('.texto_1').hide()
        $('.texto_2').hide()
        $('.texto_3').show()
        $(this).css('background-color', '#FFCA28')
        $('.show_texto_1').css('background-color', '#4DD0E1')
        $('.show_texto_2').css('background-color', '#4DD0E1')
      })
  },
  updated() {
    this.$aosRefresh()
  },
  methods: {
    primer__paso() {},
  },
}
</script>
<style lang="sass">
.image_floating
  filter: drop-shadow(19px 14px 5px rgba(0,0,0,.25))
.titulo-principal__numero span
  color: #31326F !important
.titulo-principal__numero
  background-color: #FFCA28 !important

@keyframes float
  0%
    filter: drop-shadow(0 5px 15px rgba(0,0,0,0.2))
    transform: translatey(0px)
  50%
    filter: drop-shadow(0 25px 15px rgba(0,0,0,0.1))
    transform: translatey(-20px)
  100%
    filter: drop-shadow(0 5px 15px rgba(0,0,0,0.2))
    transform: translatey(0px)
.imagen_flotante_animada
  filter: drop-shadow(0 5px 15px rgba(0,0,0,0.2))
  transform: translatey(0px)
  animation: float 6s ease-in-out infinite
.caja_flotante
  -webkit-box-shadow: -11px 10px 0px -1px #f3f3f3
  -moz-box-shadow: -11px 10px 0px -1px #f3f3f3
  box-shadow: -11px 10px 0px -1px #f3f3f3
.caja_escalada_hover
  transition: transform 0.5s linear
  -o-transition: transform 0.5s linear
  -ms-transition: transform 0.5s linear
  -moz-transition: transform 0.5s linear
  -webkit-transition: transform 0.5s linear
.caja_escalada_hover:hover
  transition: transform .5s ease
  transform: scale(1.06)
.fade-in-image
  animation: fadeIn 3s
  -webkit-animation: fadeIn 3s
  -moz-animation: fadeIn 3s
  -o-animation: fadeIn 3s
  -ms-animation: fadeIn 3s
@keyframes fadeIn
  0%
    opacity: 0
  100%
    opacity: 1
.tarjeta--azul
  background-color: #DBFBFF !important
.tarjeta-avatar-b > img
  min-width: 16%
  max-width: 16%
  top: -9%
.caja_flotante_azul
  box-shadow: -11px 10px 0px -1px #f1fcfd
.caja_flotante_rosada
  box-shadow: -11px 10px 0px -1px #fff6f6
.cajon.color-acento-botones
  background-color: #FFE7C4
.lista-ol--separador li, .lista-ul--separador li
  border-bottom: none !important
.bloque-texto-a
  background-color: #F3F9FF !important
.item_round
  background-color: rgb(255, 202, 40)
  padding: 7px 17px 7px 17px
  font-size: 33px
  font-weight: bold
  border-radius: 50%
  cursor: pointer
  transition: transform 0.5s linear
  -o-transition: transform 0.5s linear
  -ms-transition: transform 0.5s linear
  -moz-transition: transform 0.5s linear
  -webkit-transition: transform 0.5s linear
.item_round:hover
  transition: transform .5s ease
  opacity: .7
.titulo-segundo:after
  border-color: #FFCA28 !important
.texto_show
  transition: transform 0.5s linear
  -o-transition: transform 0.5s linear
  -ms-transition: transform 0.5s linear
  -moz-transition: transform 0.5s linear
  -webkit-transition: transform 0.5s linear
</style>
