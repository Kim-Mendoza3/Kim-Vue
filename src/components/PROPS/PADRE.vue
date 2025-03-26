<script setup>
// Importamos las dependencias necesarias de Vue
import { ref } from 'vue';
// Importamos los componentes hijos
import hijo1 from './HIJO1.vue';
import hijo2 from './HIJO2.vue';

// Definimos las propiedades que el componente padre puede recibir
defineProps({
    nombre: String
});
</script>

<template>
    <head>
        <!-- Importamos los iconos de Bootstrap -->
        <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons/font/bootstrap-icons.css">
    </head>
    <div class="container">
        <!-- Encabezado del componente padre con un icono -->
        <h1 class="titulo">
            <i class="bi bi-person-circle icon"></i> Soy El Componente Padre
        </h1>
        <!-- Compilamos los componentes hijos y les pasamos la propiedad 'edad' -->
        <hijo1 class="mt-4" edad="11"/>
        <hijo2 class="mt-4" edad="5"/>
    </div>
</template>

<style scoped>
/* Estilos para el encabezado del componente padre */
.titulo {
    font-family: 'Times New Roman', Times, serif; /* Tipo de letra */
    color: brown; /* Color del texto */
    display: flex; /* Para alinear el icono con el texto */
    align-items: center;
    gap: 8px; /* Espaciado entre el icono y el texto */
}

/* Estilos para el icono */
.icon {
    font-size: 24px; /* Tamaño del icono */
}
</style>
