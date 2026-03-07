<template>
  <div class="container mt-4">
    <AppHeader
      titulo="Bienvenido a Mi Sitio Web"
      imagen="https://www.salyroca.es/media/salyroca/images/2020/06/24/2020062410124155946.jpg"
    />

  <div class="row mt-4">
    <div class="col-md-5">
      <TarjetaConImagen
        titulo="Título de la Tarjeta 1"
        texto="Texto de la tarjeta 1"
        :randomInicial="1"
      />
  </div>

  <div class="col-md-5">
      <TarjetaConImagen
        titulo="Título de la Tarjeta 2"
        texto="Texto de la tarjeta 2"
        :randomInicial="2"
      />
    </div>

  </div>

  <TablaDeDatos/>

  <div class="text-center mt-4">
    <button class="btn mi-boton">
      Enviar
    </button>
  </div>

  <AppFooter/>

  </div>

</template>

<script setup>
  import AppHeader from "./components/AppHeader.vue"
  import TarjetaConImagen from "./components/TarjetaConImagen.vue"
  import TablaDeDatos from "./components/TablaDeDatos.vue"
  import AppFooter from "./components/AppFooter.vue"
</script>