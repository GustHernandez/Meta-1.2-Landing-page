<template>
    <!-- Encabezado del sitio web -->
    <AppHeader
        titulo="Bienvenido a Mi Sitio Web"
        imagen="https://www.salyroca.es/media/salyroca/images/2020/06/24/2020062410124155946.jpg"
    />
    <!-- Contenedor principal -->
    <div class="container">

        <div class="fila">
            <div class="columna">
            <!-- Primera tarjeta -->
            <TarjetaConImagen
                titulo="Titulo de la tarjeta 1"
                texto="Este es un texto descriptivo para la tarjeta 1."
                :randomInicial="1"
            />
        </div>

        <div class="columna">
            <!-- Segunda tarjeta -->
            <TarjetaConImagen
                titulo="Titulo de la tarjeta 2"
                texto="Este es un texto descriptivo para la tarjeta 2."
                :randomInicial="2"
            />
        </div>
    </div>
    <!-- Tabla de datos -->
    <TablaDeDatos />    
    <!-- Botón -->        
    <button class="boton"> Enviar </button>
    </div>
  <AppFooter />
</template>

<script setup> 
    /* Importación de los componentes utilizados en la página */
    import AppHeader from "@/components/AppHeader.vue"
    import TarjetaConImagen from "@/components/TarjetaConImagen.vue"
    import TablaDeDatos from "@/components/TablaDeDatos.vue"
    import AppFooter from "@/components/AppFooter.vue"
</script>