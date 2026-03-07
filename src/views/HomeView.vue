<template>
    <AppHeader
        titulo="Bienvenido a Mi Sitio Web"
        imagen="https://www.salyroca.es/media/salyroca/images/2020/06/24/2020062410124155946.jpg"
    />

    <v-container>
        <v-row class="mt-4">
            <v-col cols="6">
                <TarjetaConImagen
                    titulo="Titulo de la tarjeta 1"
                    texto="Este es un texto descriptivo para la tarjet 1. Puedes agregar cualquier contenido que desees aquí"
                    :randomInicial="1"
                />
            </v-col>

            <v-col cols="6">
                <TarjetaConImagen 
                    titulo="Titulo de la tarjeta 2"
                    texto="Este es un texto descriptivo para la tarjet 2. Puedes agregar cualquier contenido que desees aquí"
                    :randomInicial="2"
                />
            </v-col>
        </v-rows>

        <TablaDeDatos />
        <v-btn class="mt-4"Enviar></v-btn>
        
    </v-container>

    <AppFooter />
</template>

<script setup>
    import AppHeader from "@/components/AppHeader.vue"
    import TarjetaConImagen from "@/components/TarjetaConImagen.vue"
    import TablaDeDatos from "@/components/TablaDeDatos.vue"
    import AppFooter from "@/components/AppFooter.vue"
</script>