<template lang="pug">
.curso-main-container.introduccion
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal
      .titulo-principal__numero
        span 3
      h1 Comandos básicos de Git

    p(data-aos="fade-up") Para trabajar con Git es importante conocer los diferentes comandos que posibilitan la creación de repositorios, a continuación, se podrá acceder a ellos a través del siguiente recurso:

    .p-5.mt-5(style="background-color:#E0FBFF")
      p(data-aos="fade-up") #[strong 1. Para inicializar un repositorio desde un directorio existente se debe usar el comando:]

      .mt-4
        .col-md-3.p-3.text-white(data-aos="fade-up" style="background-color:#21214B;") 
          p.mb-0(style="font-family:Inconsolata;font-size: 1.2rem;text-shadow: 0px 0px 2px black;padding-left:12px;word-break: break-all;") $ git init

      p.mt-5(data-aos="fade-up") #[strong 2. Este comando creará un nuevo subdirectorio llamado .git, el cual contendrá todos los archivos necesarios para el repositorio. Si se desea obtener una copia desde un repositorio existente se debe utilizar el comando de clonación]

      .mt-4
        .col-md-7.p-3.text-white(data-aos="fade-up" style="background-color:#21214B;") 
          p.mb-0(style="font-family:Inconsolata;font-size: 1.2rem;text-shadow: 0px 0px 2px black;padding-left:12px;word-break: break-all;") $ git clone https://url_del_repositorio

      p.mt-5(data-aos="fade-up") #[strong 3. Este comando permite recibir una copia de casi todos los archivos existentes en el repositorio de origen, incluyendo cada versión de cada uno de los archivos. Así, si el servidor original llegara a dañarse se podrá realizar una restauración a partir de todos los clones generados.]

      p.mt-3(data-aos="fade-up") #[strong Una vez se dispone de un espacio de trabajo inicializado, se debe tener en cuenta que todos los archivos van a tener dos posibles estados, los cuales son:]

      ul.mt-4(style="list-style: disc;padding: revert;")
        li(data-aos="fade-right") #[strong Rastreados (tracked files):] son todos aquellos archivos que estaban en la última versión del proyecto independiente de si estos archivos están modificados, sin modificar o preparados. Cuando se clona un proyecto a partir de un repositorio existente, todos estos archivos pertenecen al estado rastreado y sin modificar. Una vez un archivo es editado pasa al estado modificado, luego se deben pasar al estado de preparación para finalmente confirmarlos.

        li(data-aos="fade-right").mt-3 #[strong Sin rastrear:] corresponden a todos aquellos archivos que no formaban parte de la última versión del proyecto y no están en el área de preparación (stagin area).

      p.mt-5(data-aos="fade-up") #[strong 4. Para visualizar el estado actual de tus archivos indicando si están o no rastreados por Git se puede ejecutar el siguiente comando:]

      .mt-4
        .col-md-3.p-3.text-white(data-aos="fade-up" style="background-color:#21214B;") 
          p.mb-0(style="font-family:Inconsolata;font-size: 1.2rem;text-shadow: 0px 0px 2px black;padding-left:12px;word-break: break-all;") $ git status

      p.mt-5(data-aos="fade-up") #[strong 5. Para todos los archivos nuevos que se desean ser rastreados por Git, se debe indicar con el siguiente comando:]

      .mt-4
        .col-md-4.p-3.text-white(data-aos="fade-up" style="background-color:#21214B;") 
          p.mb-0(style="font-family:Inconsolata;font-size: 1.2rem;text-shadow: 0px 0px 2px black;padding-left:12px;word-break: break-all;") $ git add Nombre_archivo

      p.mt-5(data-aos="fade-up") #[strong 6. También es posible indicar a Git que haga rastreo de un directorio, lo cual implica que recursivamente se hace rastreo de todos los archivos en el interior del directorio.]

      .mt-4
        .col-md-4.p-3.text-white(data-aos="fade-up" style="background-color:#21214B;") 
          p.mb-0(style="font-family:Inconsolata;font-size: 1.2rem;text-shadow: 0px 0px 2px black;padding-left:12px;word-break: break-all;") $ git add Directorio

      p.mt-5(data-aos="fade-up") #[strong 7. El comando git add además de servir para iniciar el rastreo de un archivo o directorio que no estaba en la última versión, también sirve para preparar archivos (enviarlos al staging area) y para marcar archivos como resueltos en los casos donde estos entran en conflictos por operaciones de combinación. Dicho de una manera más simplificada: el comando add indica que un archivo o directorio debe ser añadido en la próxima confirmación. Para confirmar cambios se ejecuta el comando:]

      .mt-4
        .col-md-3.p-3.text-white(data-aos="fade-up" style="background-color:#21214B;") 
          p.mb-0(style="font-family:Inconsolata;font-size: 1.2rem;text-shadow: 0px 0px 2px black;padding-left:12px;word-break: break-all;") $ git commit

      p.mt-5(data-aos="fade-up") #[strong 8. Al ejecutar la confirmación el sistema desplegará un mecanismo para recibir un mensaje de confirmación que será asociado a esta operación de commit. También es posible agregar el comentario explícitamente en la ejecución de la confirmación usando la opción -m.]

      .mt-4
        .col-md-8.p-3.text-white(data-aos="fade-up" style="background-color:#21214B;") 
          p.mb-0(style="font-family:Inconsolata;font-size: 1.2rem;text-shadow: 0px 0px 2px black;padding-left:12px;word-break: break-all;") $ git commit -m “En esta version se arreglo el archive W”

      p.mt-5(data-aos="fade-up") #[strong 9. También es posible ejecutar una operación de confirmación que salte el paso de preparación que se logra con la ejecución del comando add. Es decir, la operación de confirmación se encarga de preparar todos los archivos rastreados y luego confirmar. Esto es posible agregando la opción -a.]

      .mt-4
        .col-md-7.p-3.text-white(data-aos="fade-up" style="background-color:#21214B;") 
          p.mb-0(style="font-family:Inconsolata;font-size: 1.2rem;text-shadow: 0px 0px 2px black;padding-left:12px;word-break: break-all;") $ git commit -a -m ‘comentario de esta confirmación’

      p.mt-5(data-aos="fade-up") #[strong 10. Para visualizar el histórico de las confirmaciones desde la más reciente hasta la más antigua realizadas sobre un repositorio se ejecuta el comando:]

      .mt-4
        .col-md-3.p-3.text-white(data-aos="fade-up" style="background-color:#21214B;") 
          p.mb-0(style="font-family:Inconsolata;font-size: 1.2rem;text-shadow: 0px 0px 2px black;padding-left:12px;word-break: break-all;") $ git log



</template>

<script>
export default {
  name: 'Tema3',
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
