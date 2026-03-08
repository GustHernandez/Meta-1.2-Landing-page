<template>
  <div class="card">
    <!-- Imagen aleatoria -->
    <img 
      :src="'https://picsum.photos/250/150?random=' + numeroRandom"
      class="imagen"
    />

    <h3>
      {{ titulo }}
    </h3>

    <p>
      {{ texto }}
    </p>
    <!-- Botón para cambiar la imagen -->
    <button @click="cambiarImagen">
      Cambiar imagen
    </button>

  </div>
</template>

<script setup>
import { ref } from "vue"

const props = defineProps({
  titulo: String,
  texto: String,
  randomInicial: Number
})
/* Numero para la imagen aleatoria */
const numeroRandom = ref(props.randomInicial)
/* Función para cambiar la imagen cuando se presione el botón */
function cambiarImagen(){
  numeroRandom.value = Math.floor(Math.random() * 1000)
}
</script>
<style>
    /* Estilo de la tarjeta */
    .card{
    border: 1px solid #ccc;
    border-radius: 10px;
    padding: 15px;
    text-align: center;
    width: 250px;
    }
    /* Estilo de la imagen */
    .imagen{
    width: 100%;
    height: 150px;
    object-fit: cover;
    }
    /* Estilo del botón */
    button{
    margin-top: 10px;
    padding: 8px 12px;
    cursor: pointer;
    }
</style>