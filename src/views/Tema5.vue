<template lang="pug">
.curso-main-container.introduccion
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal
      .titulo-principal__numero
        span 5
      h1 Plataformas para implementar integración continua - Gitlab

    p(data-aos="fade-up") En la actualidad existe gran cantidad de plataformas con servicios en la nube en los que se pueden implementar procesos de integración continua, los cuales, generalmente, ofrecen la posibilidad de crear repositorios públicos y privados, se integran con sistemas de control de versiones, permiten el registro de grupos de trabajo y otras posibilidades más. Entre los más utilizados en la industria que se basan en sistemas de control de versiones en Git, se encuentran los descritos a continuación:

    br
    br
    .row.mt-5
      .col-md-4.mb-5
        .p-5.text-center.m-auto.caja_flotante_azul.caja_escalada_hover(style="background-color:#F3F9FF;height:100%;")
          figure
            img.imagen_flotante_animada.m-auto(src="@/assets/curso/tema5/1.svg" style="margin-top:-8rem !important;width:150px;")
          h4.mt-5 GitHub
          p #[strong Conoce GitHub un portal creado para alojar códigos de las aplicaciones.]

          .mt-5
            a.h5(href="https://Github.com" target="_blank")
              i.fas.fa-link(style="background-color: #4DD0E1;color: white;padding: 7px;")
              |  https://Github.com

      .col-md-4.mb-5
        .p-5.text-center.m-auto.caja_flotante_azul.caja_escalada_hover(style="background-color:#F3F9FF;height:100%;")
          figure
            img.imagen_flotante_animada.m-auto(src="@/assets/curso/tema5/2.svg" style="margin-top:-8rem !important;width:150px;")
          h4.mt-5 GitLab
          p #[strong Conoce sobre GitLab, un servicio web que permite controlar las versiones y desarrollos de software colaborativo basado en Git.]

          .mt-5
            a.h5(href="https://about.Gitlab.com" target="_blank")
              i.fas.fa-link(style="background-color: #4DD0E1;color: white;padding: 7px;")
              |  https://about.Gitlab.com

      .col-md-4.mb-5
        .p-5.text-center.m-auto.caja_flotante_azul.caja_escalada_hover(style="background-color:#F3F9FF;height:100%;")
          figure
            img.imagen_flotante_animada.m-auto(src="@/assets/curso/tema5/3.svg" style="margin-top:-8rem !important;width:150px;")
          h4.mt-5 BitBucket
          p #[strong Conoce a Bitbucket un servicio de alojamiento basado en web para los proyectos que utilizan sistema de control de versiones Mercurial y Git.]

          .mt-5
            a.h5(href="https://bitbucket.org" target="_blank")
              i.fas.fa-link(style="background-color: #4DD0E1;color: white;padding: 7px;")
              |  https://bitbucket.org



    p.mt-3(data-aos="fade-up") Para complementar la información sobre los anteriores sistemas, a continuación, se podrá conocer sobre las diferentes versiones gratuitas con sus funcionalidades básicas, las cuales son accesibles simplemente con la creación de una cuenta de usuario.

    .titulo-quinto.color-acento-contenido.mt-5(data-aos="fade-up")
      h4 Plataformas para implementar integración continua – Gitlab

    div.mt-5.indicador__container(active="true")
      b-card(no-body='')
        b-tabs(pills='' card='' vertical='')
          b-tab(disabled="true")
            template(#title)
              h3.text-center.mb-0.pb-4.pt-4(style="color:#1565C0;") Proceso para crear un repositorio #[br] en la plataforma Gitlab
              .indicador--click
          b-tab
            template(#title)
              div.pt-3(style="border-top:1px #B2E6FF solid;")
                i.fas.fa-caret-right
                |  Creación de cuenta
            b-card-text
              figure
                img(src="@/assets/curso/tema5/5.png")
                figcaption Creación de cuenta
              .p-4.mt-2.caja_flotante(data-aos="fade-up" style="background-color:#F6F6F6;")
                p Primero se debe crear una cuenta en Gitlab directamente desde el enlace: #[a(href="https://gitlab.com/users/sign_up") https://gitlab.com/users/sign_up]

                p.mt-3 El proceso se puede realizar de forma tradicional o usando cuentas ya existentes de otras plataformas como Google, Github, Twitter, Bitbucket o Salesforce.

          b-tab
            template(#title)
              div.pt-3(style="border-top:1px #B2E6FF solid;")
                i.fas.fa-caret-right
                |  Aceptación de términos de servicios
            b-card-text
              figure
                img(src="@/assets/curso/tema5/6.png")
                figcaption Aceptación de términos de servicios
              .p-4.mt-2.caja_flotante(data-aos="fade-up" style="background-color:#F6F6F6;")
                p Una vez se realiza el registro se debe aceptar los términos del servicio y las políticas de privacidad.

          b-tab
            template(#title)
              div.pt-3(style="border-top:1px #B2E6FF solid;")
                i.fas.fa-caret-right
                |  Interfaz de inicio
            b-card-text
              figure
                img(src="@/assets/curso/tema5/7.png")
                figcaption Interfaz de inicio
              .p-4.mt-2.caja_flotante(data-aos="fade-up" style="background-color:#F6F6F6;")
                p Después de esto, se muestra la interfaz de inicio donde se puede crear directamente el proyecto (repositorio).

          b-tab
            template(#title)
              div.pt-3(style="border-top:1px #B2E6FF solid;")
                i.fas.fa-caret-right
                |  Creación de proyecto
            b-card-text
              figure
                img(src="@/assets/curso/tema5/8.png")
                figcaption Creación de proyecto
              .p-4.mt-2.caja_flotante(data-aos="fade-up" style="background-color:#F6F6F6;")
                p En la parte de creación de proyectos, se ofrecen cuatro posibilidades: creación de proyecto en blanco, creación de proyecto desde plantilla, importar proyectos desde otros sistemas o conectar repositorios externos con GitLab CI/CD. Para el caso de grupos de desarrollo que apenas inician con prácticas de integración continua el proyecto en blanco es la mejor opción.

          b-tab
            template(#title)
              div.pt-3(style="border-top:1px #B2E6FF solid;")
                i.fas.fa-caret-right
                |  Nombre del proyecto
            b-card-text
              figure
                img(src="@/assets/curso/tema5/9.png")
                figcaption Nombre del proyecto
              .p-4.mt-2.caja_flotante(data-aos="fade-up" style="background-color:#F6F6F6;")
                p A continuación, se debe definir el nombre del proyecto, se puede agregar una descripción y se define el tipo de visibilidad que puede ser pública (cualquiera podría acceder sin autenticarse) o privada (debe tener permisos asignados para ingresar).

                p.mt-3 Note que la URL asignada dependerá del nombre de usuario asignado a la cuenta de Gitlab creada y el nombre definido al repositorio.

          b-tab
            template(#title)
              div.pt-3(style="border-top:1px #B2E6FF solid;")
                i.fas.fa-caret-right
                |  Instrucción de uso
            b-card-text
              figure
                img(src="@/assets/curso/tema5/10.png")
                figcaption Instrucción de uso
              .p-4.mt-2.caja_flotante(data-aos="fade-up" style="background-color:#F6F6F6;")
                p Una vez finalizado el proceso el sistema le recuerda un conjunto de instrucciones para usar el repositorio entre las cuales se encuentra la configuración del usuario y correo de acuerdo con las credenciales de Gitlab y los comandos Git para hacer su respectiva gestión.

                p.mt-3 A continuación, lo único que queda por hacer es conectar el equipo local con el repositorio remoto por medio de Git usando los comandos vistos anteriormente.

                p.mt-3 En este caso se usará la ayuda ofrecida por Gitlab para crear un nuevo repositorio local realizando la clonación respectiva desde el repositorio remoto.

          b-tab
            template(#title)
              div.pt-3(style="border-top:1px #B2E6FF solid;")
                i.fas.fa-caret-right
                |  Modificación de usuario
            b-card-text
              figure
                img(src="@/assets/curso/tema5/11.png")
                figcaption Modificación de usuario
              .p-4.mt-2.caja_flotante(data-aos="fade-up" style="background-color:#F6F6F6;")
                p En primer lugar, se debe modificar el usuario y la cuenta de correo en la máquina local para que coincida con las credenciales autorizadas en el repositorio remoto.

          b-tab
            template(#title)
              div.pt-3(style="border-top:1px #B2E6FF solid;")
                i.fas.fa-caret-right
                |  Clonación de repositorio
            b-card-text
              figure
                img(src="@/assets/curso/tema5/12.png")
                figcaption Clonación de repositorio
              .p-4.mt-2.caja_flotante(data-aos="fade-up" style="background-color:#F6F6F6;")
                p Luego, se clona el repositorio creado en Gitlab para copiarlo en la máquina local, en este punto debe tener claridad sobre el usuario y su contraseña en Gitlab ya que esta será preguntada en el proceso de clonación.

                p.mt-3 Una vez se verifican las credenciales se hace el proceso de clonación, en este caso es un repositorio vacío, pero se encontrará en el sistema local de archivos una carpeta con el mismo nombre definido en el repositorio remoto con toda la configuración para hacer la respectiva gestión de estados con git. Este repositorio se convierte en el directorio de trabajo local.

          b-tab
            template(#title)
              div.pt-3(style="border-top:1px #B2E6FF solid;")
                i.fas.fa-caret-right
                |  Acceso al directorio
            b-card-text
              figure
                img(src="@/assets/curso/tema5/13.png")
                figcaption Acceso al directorio
              .p-4.mt-2.caja_flotante(data-aos="fade-up" style="background-color:#F6F6F6;")
                p Ahora se accede al directorio de trabajo para empezar la construcción de archivos, ponerlos en rastreo, prepararlos, confirmarlos localmente y luego enviar la versión confirmada localmente al repositorio remoto. Se debe utilizar el comando git switch -c nombre para crear una nueva rama de trabajo local, donde el nombre corresponde al nombre de la rama.

          b-tab
            template(#title)
              div.pt-3(style="border-top:1px #B2E6FF solid;")
                i.fas.fa-caret-right
                |  Creación de archivo local
            b-card-text
              figure
                img(src="@/assets/curso/tema5/14.png")
                figcaption Creación de archivo local
              .p-4.mt-2.caja_flotante(data-aos="fade-up" style="background-color:#F6F6F6;")
                p Después de esto se probará crear un archivo local vacío llamado README.md el cual se preparará, confirmará y enviará al repositorio remoto.

          b-tab
            template(#title)
              div.pt-3(style="border-top:1px #B2E6FF solid;")
                i.fas.fa-caret-right
                |  Archivo de rastreo
            b-card-text
              figure
                img(src="@/assets/curso/tema5/15.png")
                figcaption Archivo de rastreo
              .p-4.mt-2.caja_flotante(data-aos="fade-up" style="background-color:#F6F6F6;")
                p Luego, se agrega este archivo para que sea rastreado y agregado al área de preparación.

          b-tab
            template(#title)
              div.pt-3(style="border-top:1px #B2E6FF solid;")
                i.fas.fa-caret-right
                |  Archivo de repositorio local
            b-card-text
              figure
                img(src="@/assets/curso/tema5/16.png")
                figcaption Archivo de repositorio local
              .p-4.mt-2.caja_flotante(data-aos="fade-up" style="background-color:#F6F6F6;")
                p Se Confirma el archivo en el repositorio local, lo cual genera una nueva versión en el repositorio local.

          b-tab
            template(#title)
              div.pt-3(style="border-top:1px #B2E6FF solid;")
                i.fas.fa-caret-right
                |  Envío al repositorio remoto
            b-card-text
              figure
                img(src="@/assets/curso/tema5/17.png")
                figcaption Envío al repositorio remoto
              .p-4.mt-2.caja_flotante(data-aos="fade-up" style="background-color:#F6F6F6;")
                p Luego de tener ya una versión confirmada se envía al repositorio remoto. Se deberá ingresar las credenciales de usuario en Gitlab.

          b-tab
            template(#title)
              div.pt-3(style="border-top:1px #B2E6FF solid;")
                i.fas.fa-caret-right
                |  Repositorio Gitlab
            b-card-text
              figure
                img(src="@/assets/curso/tema5/18.png")
                figcaption Repositorio Gitlab
              .p-4.mt-2.caja_flotante(data-aos="fade-up" style="background-color:#F6F6F6;")
                p En este punto los cambios aplicados ya se pueden visualizar directamente desde la plataforma Gitlab.

          b-tab
            template(#title)
              div.pt-3(style="border-top:1px #B2E6FF solid;")
                i.fas.fa-caret-right
                |  Agregar colaboradores
            b-card-text
              figure
                img(src="@/assets/curso/tema5/19.png")
                figcaption Agregar colaboradores
              .p-4.mt-2.caja_flotante(data-aos="fade-up" style="background-color:#F6F6F6;")
                p Para agregar colaboradores que puedan también clonar, preparar, confirmar y subir cambios al repositorio es necesario agregarlos como colaboradores y asignarles los permisos requeridos ya que el repositorio fue definido como privado.

                p.mt-3 Para eso, se debe regresar a gitlab y sobre el menú del panel del lado izquierdo se selecciona la opción de información del proyecto y luego miembros.

          b-tab
            template(#title)
              div.pt-3(style="border-top:1px #B2E6FF solid;")
                i.fas.fa-caret-right
                |  Configuración de roles
            b-card-text
              figure
                img(src="@/assets/curso/tema5/20.png")
                figcaption Configuración de roles
              .p-4.mt-2.caja_flotante(data-aos="fade-up" style="background-color:#F6F6F6;")
                p Por defecto, el usuario creador del repositorio aparece como miembro de este. Por medio de esta interfaz se puede invitar a nuevos miembros por medio de correo electrónico o por nombre de usuario si ya están registrados en Gitlab. Adicionalmente, se puede configurar el rol asociado a este usuario e incluso definir fecha en la cual expira la autorización asignada. Si se desea asignar permisos de lectura y escritura se recomienda asignar el rol Mainteiner.

                p.mt-3 Usando este mismo espacio se pueden revocar permisos y eliminar colaboradores del proyecto.

                p.mt-3 Todos los usuarios autorizados podrán realizar clonación del repositorio e interactuar con él por medio de los comandos Git vistos a lo largo de este módulo.




</template>

<script>
export default {
  name: 'Tema5',
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
.anexo *
  color: #12263f !important
.card
  border:0 !important
.card-header
  background-color: #F3F9FF !important
.nav-link
  color: #1565C0 !important
  background-color: #f3f9ff !important
  border-top: 1px #B2E6FF solid !important
  border-radius: 0px !important
.nav-pills
  border-top: 9px #B4E2F8 solid !important
.nav-link:first-child
  border-top:0px !important
.nav-link.active
  font-weight:bold !important
.card-body
  padding: 0px
</style>
