<template>
    <v-card class="text-center">
        <v-img 
        :src="imagen"
        height="300"
        cover
        />

        <v-card-title class="text-h4">
        {{ titulo }}
        </v-card-title>

    </v-card>
</template>

<script setup>
defineProps({
    titulo: String, 
    imange: String
})
</script>