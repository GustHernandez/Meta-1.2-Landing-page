<template>
    <v-table>
        <thead>
            <th v-for="dato in datos":key="dato">
                {{ dato }}
            </th>
        </tr>
    </thead>
    
    <tbody>
        <tr v-for="(fila,index) in filas": key="index">
            <td v-for="(valor, i) in fila":key="i">
                {{ valor }}

            </td>
        </tr>
    </tbody>
    </v-tables>
</template>

<script setup>

const datos = [
    "Columna 1", 
    "Columna 2",
    "Columna 3"
]

const filas = [
    ["Valor 1", "Valor 2", "Valor 3"],
    ["Valor 4", "Valor 5", "Valor 6"]
]

</script>