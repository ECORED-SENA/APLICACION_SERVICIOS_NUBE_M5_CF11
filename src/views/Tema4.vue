<template lang="pug">
.curso-main-container.introduccion
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal
      .titulo-principal__numero
        span 4
      h1 Git en entornos remotos

    p(data-aos="fade-up") Para poder colaborar con un equipo de trabajo e implementar el concepto de integración continua, es necesario hospedar los proyectos en repositorios remotos los cuales son accesibles por medio de internet o por un entorno de red.

    p.mt-3(data-aos="fade-up") En estos repositorios remotos se definen una serie de permisos que indican si se tiene la posibilidad de leer o de lectura y escritura. El colaborar implica la gestión de estos repositorios enviando y obteniendo información desde estos, teniendo en cuenta los estados que ya se han mencionado anteriormente. Se podrá acceder a ellos mediante: 

    p.mt-3(data-aos="fade-up") #[strong A continuación, se relacionan los pasos a seguir para los entornos remotos.]

    .p-5.mt-5(style="background-color:#E0FBFF")
      p(data-aos="fade-up") #[strong 1. Para ver los repositorios remotos configurados se puede ejecutar el comando:]

      .mt-4
        .col-md-3.p-3.text-white(data-aos="fade-up" style="background-color:#21214B;") 
          p.mb-0(style="font-family:Inconsolata;font-size: 1.2rem;text-shadow: 0px 0px 2px black;padding-left:12px;word-break: break-all;") $ git remote

      p.mt-5(data-aos="fade-up") #[strong 2. Para definir un repositorio remoto y asociarlo a un nombre para su referenciación se utiliza el siguiente comando:]

      .mt-4
        .col-md-5.p-3.text-white(data-aos="fade-up" style="background-color:#21214B;") 
          p.mb-0(style="font-family:Inconsolata;font-size: 1.2rem;text-shadow: 0px 0px 2px black;padding-left:12px;word-break: break-all;") git remote add [nombre-remoto] [url]

      p.mt-5(data-aos="fade-up") #[strong 3. Donde nombre-remoto corresponde al nombre con que se referencia el repositorio y URL es la ubicación lógica del mismo en un entorno de red o en una dirección de internet. En el siguiente ejemplo se define un repositorio ubicado en un servidor de Github y cuyo nombre de referencia es ref.]

      .mt-4
        .col-md-8.p-3.text-white(data-aos="fade-up" style="background-color:#21214B;") 
          p.mb-0(style="font-family:Inconsolata;font-size: 1.2rem;text-shadow: 0px 0px 2px black;padding-left:12px;word-break: break-all;") $ git remote add ref https://github.com/paulboone/ticgit

      p.mt-5(data-aos="fade-up") #[strong 4. Una vez definido el remote se pueden extraer los datos utilizando el siguiente comando:]

      .mt-4
        .col-md-4.p-3.text-white(data-aos="fade-up" style="background-color:#21214B;") 
          p.mb-0(style="font-family:Inconsolata;font-size: 1.2rem;text-shadow: 0px 0px 2px black;padding-left:12px;word-break: break-all;") $ git fetch [nombre-remoto]

      p.mt-5(data-aos="fade-up") #[strong 5. El anterior comando se conecta al repositorio remoto y trae todos los datos de los cuales aún no se tiene copia en tu repositorio local. Para enviar información desde el repositorio local hacia el servidor remoto, se utiliza el siguiente comando:]

      .mt-4
        .col-md-6.p-3.text-white(data-aos="fade-up" style="background-color:#21214B;") 
          p.mb-0(style="font-family:Inconsolata;font-size: 1.2rem;text-shadow: 0px 0px 2px black;padding-left:12px;word-break: break-all;") git push [nombre-remoto] [nombre-rama]

      p.mt-5(data-aos="fade-up") #[strong 6. Recordemos que, si se ha clonado un repositorio desde alguna ubicación, Git asigna el nombre origin al servidor del que se ha realizado la clonación. Así, si por ejemplo queremos enviar nuestra rama master al servidor origin se debe ejecutar el comando de la siguiente forma:]

      .mt-4
        .col-md-4.p-3.text-white(data-aos="fade-up" style="background-color:#21214B;") 
          p.mb-0(style="font-family:Inconsolata;font-size: 1.2rem;text-shadow: 0px 0px 2px black;padding-left:12px;word-break: break-all;") $ git push origin master

</template>

<script>
export default {
  name: 'Tema4',
  data: () => ({
    mostrarIndicador: true,
    modal1: false,
  }),
  mounted() {
    this.$nextTick(() => {
      this.$aosRefresh()
    })
  },
  updated() {
    this.$aosRefresh()
  },
  methods: {},
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
@font-face
  font-family: "Inconsolata"
  src: url("/fonts/Inconsolata-VariableFont_wdth,wght.ttf")
</style>
