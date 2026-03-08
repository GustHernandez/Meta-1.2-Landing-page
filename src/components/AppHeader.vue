<template>
    <!-- Contenedor principal del encabezado-->
    <div class="header">
        <!-- Imagen del encabezado -->
        <img 
        :src="imagen"
        class="imagen"
    />
    <!-- Titulo de la pagina -->
    <h1 class="titulo">
      {{ titulo }}
    </h1>
    </div>
</template>

<script setup>
    /* Definición de propiedades que recibe el componente */
    defineProps({
    titulo: String,
    imagen: String
    })
</script>

<style>
    /* Contenedor del header */
    .header{
    position: relative;
    text-align: center;
    }
 
    /* Estilo de la imagen del encabezado */
    .imagen{
    width: 100%;
    height: 300px;
    object-fit: cover;
    }
    /* Estilo del titulo sobre la imagen  */
    .titulo{
    position: absolute;
    top: 30%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: white;
    font-size: 40px;
    padding: 10px 20px;
    border-radius: 10px;
    }
</style>