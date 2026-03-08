<template>
    <!-- Tabla que muestra los datos-->
    <table class="tabla">
        <!-- encabezado de la tabla -->
        <thead>
            <tr>
                <!-- Se recorre el arreglo de datos para crear las columnas-->
                <th v-for="dato in datos" :key="dato">
                    {{ dato }}
                </th>
            </tr>
        </thead>
        <!-- Cuerpo de la tabla-->
        <tbody>
            <!-- Se recorren las filas -->
            <tr v-for="(fila, index) in filas" :key="index">
                <!-- Se recorren los valores de cada fila -->
                <td v-for="(valor, i) in fila" :key="i">
                    {{ valor }}

                </td>
            </tr>
        </tbody>
    </table>
</template>

<script setup>
/* 
 * Nombres de las columnas 
 */
const datos = [
    "Columna 1",
    "Columna 2",
    "Columna 3"
]
/* 
 * Valores de cada fila
 */
const filas = [
    ["Valor 1", "Valor 2", "Valor 3"],
    ["Valor 4", "Valor 5", "Valor 6"]
]
</script>

<style> 
    /* Estilo de la tabla */
    .tabla{
        width: 100%;
        border-collapse: collapse; 
        margin-top: 20px; 
        background-color: #af7b1a;
    }
    /* Estilo de las celdas y encabezados */
    .tabla th, .tabla td{
        border: 1px solid #000000;
        padding: 10px; 
        text-align: center;
    }
    
    .tabla th{
        background-color: #d78819;
    }
</style>