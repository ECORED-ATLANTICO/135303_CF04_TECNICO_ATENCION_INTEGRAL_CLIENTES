<template lang="pug">
.curso-main-container.introduccion
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal.color-acento-contenido
      .titulo-principal__numero
        span
          i.fas.fa-info
      h1 Introducción
    
    p.mb-3 ¡Bienvenido al componente Gestión de requerimientos e indicadores de gestión! En esta introducción se presenta un acercamiento a los protocolos de servicio al cliente, su importancia en la atención de los usuarios y las pautas que orientan la gestión de sus necesidades y requerimientos.
    p.mb-3 Este recurso permite reconocer los elementos fundamentales para brindar una atención oportuna y garantizar un servicio de calidad.

    .titulo-sexto.color-acento-contenido.mb-4
      h5 Video 1.
      span Protocolos de servicio al cliente introducción

    figure.mb-5
      .video-mb-2(data-aos="fade-up")
        iframe(width="100%" height="560" src="https://www.youtube.com/embed/lvRg5NSUEIo?si=tt7B8aiU2lk6yxbi" title="Video: Gestión de requerimientos e indicadores de gestión" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen)

</template>

<script>
export default {
  name: 'Introduccion',
  data: () => ({
    // variables de vue
  }),
  mounted() {
    this.$nextTick(() => {
      this.$aosRefresh()
    })
  },
  updated() {
    this.$aosRefresh()
  },
}
</script>

<style lang="sass"></style>
