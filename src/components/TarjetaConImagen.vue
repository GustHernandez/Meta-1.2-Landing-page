<template>
    <v-card>
        <v-img 
            :src="'https://picsum.photos/250/150?random=' + numeroRandom"
            height="150"
        />

        <v-card-title>
            {{ titulo }}
        </v-card-title>

        <v-card-text>
            {{ texto }}
        </v-card-text>

        <v-btn @click="cambiarImagen">Cambiar imagen </v-btn>
    </v-card>
</template>

<script setup>
import { ref } from "vue"
const props = defineProps({
    titulo: String,
    texto: String,
    randomInicial: Number
})

const numeroRandom = ref(props.randomInicial)

function cambiarImagen(){
    numeroRandom.value = Math.floor(Math.random()*1000);
}
</script>
