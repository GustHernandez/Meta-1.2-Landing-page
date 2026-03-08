<template>
  <div>
    <!-- Componente del encabezado de la página -->
    <AppHeader
      titulo="Bienvenido a Mi Sitio Web"
      imagen="https://www.salyroca.es/media/salyroca/images/2020/06/24/2020062410124155946.jpg"
    />

    <div class="contenedor-tarjetas">
      <!-- Primera tarjeta con imagen, titulo y descripción -->
      <TarjetaConImagen
        titulo="Tarjeta 1"
        texto="Este es un texto descriptivo para la tarjeta 1. Puedes agregar cualquier contenido que desees aquí"
        :randomInicial="1"
      />
      <!-- Segunda tarjeta con imagen, titulo y descripción -->
      <TarjetaConImagen
        titulo="Tarjeta 2"
        texto="Este es un texto descriptivo para la tarjeta 2. Puedes agregar cualquier contenido que desees aquí"
        :randomInicial="2"
      />
    </div>
    <!-- Componente que muestra la tabla de datos -->
    <TablaDeDatos />
    <!-- Botón debajo de la tabla -->
    <div class= "boton-container">
      <button class="boton">Enviar</button>
    </div>
    <AppFooter />
  </div>
</template>

<script setup>
  /* Importación de los componentes utilizados en la página */
  import AppHeader from "./components/AppHeader.vue"
  import TarjetaConImagen from "./components/TarjetaConImagen.vue"
  import TablaDeDatos from "./components/TablaDeDatos.vue"
  import AppFooter from "./components/AppFooter.vue"
</script>

<style>
  /* Estilo del contenedor de tarjetas */
  .contenedor-tarjetas{
    display: flex;
    gap: 20px;
    justify-content: center;
    margin-top: 20px;
  }
  /* Estilo del botón*/
  .boton-container{
      text-align: center;
      margin-top: 10px;
  }
  .boton{
    padding: 10px 20px;
    font-size: 16px; 
    background-color: #e3a023;
    color: white;
    border: none;
    border-radius: 6px;
    cursos: pointer;
  }
  .boton:hover{
    background-color: #bf800a;
  }
</style>