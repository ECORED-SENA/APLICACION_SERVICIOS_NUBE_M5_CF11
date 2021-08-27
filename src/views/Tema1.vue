<template lang="pug">
.curso-main-container.introduccion
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal
      .titulo-principal__numero
        span 1
      h1 Sistemas de control de versiones

    p(data-aos="fade-up") Un sistema de control de versiones se encarga del registro de los cambios realizados a lo largo del tiempo en uno o un conjunto de archivos (versiones), de forma tal que estos puedan ser recuperados con precisión de acuerdo a las necesidades de los usuarios. A este tipo de procesos se le puede denominar versionamiento y si bien este tipo de actividades son comunes en archivos o código fuente en la industria del desarrollo de software, este es un proceso aplicable a cualquier tipo de archivo.

    .mt-5.p-5(style="background-color:#4DD0E1;border-radius:10px;")
      p(data-aos="fade-up") El proceso de hacer copias de seguridad y crear versiones de los archivos que se consideran importantes es una actividad muy común, así, por medio del uso de un sistema de control de versiones se obtienen gran cantidad de posibilidades entre las que se encuentran:
      figure.mt-5
        img.imagen_flotante_animada(data-aos="fade-up" src="@/assets/curso/tema1/1.svg")

    p.mt-5(data-aos="fade-in") Respecto a los sistemas de control de versiones estos pueden ser categorizados según sus características en tres grupos: sistemas de control de versiones locales, sistemas de control de versiones centralizados y sistemas de control de versiones distribuidos.

    p.mt-3 #[strong A continuación, se podrán conocer sobre los sistemas de control de versiones locales, centralizadas y distribuidas:]

    SlyderB.mt-5(:datos="datosSlyder")

</template>

<script>
export default {
  name: 'Tema1',
  data: () => ({
    mostrarIndicador: true,
    modal1: false,
    datosSlyder: [
      {
        titulo: 'Sistemas de control de versiones locales',
        texto:
          'Una forma de llevar control de versiones locales es el crear copias manuales en un directorio exclusivo o de fácil reconocimiento donde llevamos registro de los cambios realizados sobre un documento particular, generalmente por medio de una numeración o inclusos llevando registro de la fecha de realización de la versión, como se ve en la figura 1.',
        imagen: require('@/assets/curso/tema1/2.png'),
      },
      {
        titulo: 'Sistemas de control de versiones locales',
        texto:
          'Lo anterior, aunque puede ser una práctica común y fácil de implementar, resultaría muy riesgosa, ya que la posibilidad de introducir errores, olvidar la ubicación del directorio, sobrescribir por accidente un archivo o nombrar de forma incorrecta un archivo es muy alta. <br></br> Para solucionar este problema aparecieron hace un tiempo los sistemas de control de versiones locales, los cuales contenían una base de datos simple donde se registraba información de todos los cambios realizados sobre los archivos como se muestra en la figura 2.',
        imagen: require('@/assets/curso/tema1/3.png'),
      },
      {
        titulo: 'Sistemas de control de versiones centralizados',
        texto:
          'Este tipo de sistemas surgen para solucionar el problema asociado a la colaboración con un grupo de trabajo, ya que bajo el sistema de control de versiones locales la única forma de colaborar en equipo era hacer un proceso de sincronización manual donde los miembros de un equipo debían sacar copias de los archivos que son procesados localmente y enviarlo a sus compañeros los cuales, manualmente, debían integrar sus propios cambios para, luego, hacer el mismo proceso de regreso. En los sistemas de control de versiones centralizados se dispone de un servidor donde se almacenan todos archivos y a partir del cual varios clientes pueden realizar descargas como se muestra en la figura 3.',
        imagen: require('@/assets/curso/tema1/4.png'),
      },
      {
        titulo: 'Sistemas de control de versiones centralizados',
        texto:
          'Este tipo de sistemas de control de versiones ha sido ampliamente utilizado en la industria del software ya que facilitan el trabajo colaborativo, permite un control detallado por parte de los administradores y es mucho más fácil de administrar en comparación con los procesos de sincronización manuales que debían realizarse en sistemas de control de versiones locales cuando se trabaja en equipo. Sin embargo, al tratarse de sistemas centralizados existe una dependencia muy peligrosa sobre del equipo central, y si este por alguna razón entra en fallo automáticamente y bloqueará a todos los usuarios y, en casos más extremos, se puede perder todo si, eventualmente, el equipo central entra en un fallo del que no se pueda recuperar como, por ejemplo, fallas en los discos.',
        imagen: require('@/assets/curso/tema1/4.png'),
      },
      {
        titulo: 'Sistemas de control de versiones centralizados',
        texto:
          'En este tipo de sistemas los clientes además de descargar una copia actual de los archivos presentes en el repositorio, crean una réplica completa del mismo, de forma que si, por alguna razón el servidor entra en fallo, los repositorios presentes en los clientes sirven para hacer el proceso de restauración. Es decir, que en estos sistemas los clientes se convierten en clones del repositorio en el servidor.<br></br> Este tipo de sistemas permiten administrar múltiples repositorios remotos con los que los usuarios pueden trabajar de manera simultánea con diferentes grupos de personas en varios proyectos e incluso dentro del mismo proyecto y de distintas formas, es decir, posibilitan el establecimiento de varios flujos de trabajo que no son posibles de implementar en sistemas centralizados y mucho menos en sistemas locales.',
        imagen: require('@/assets/curso/tema1/5.png'),
      },
    ],
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
.slyder-b__slyde img
  max-height: 500px !important
</style>
