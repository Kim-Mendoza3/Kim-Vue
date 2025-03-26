<script setup>
// Importamos ref de Vue (aunque no se usa en este código, podría ser útil en futuras modificaciones)
import { ref } from 'vue';

// Definimos las propiedades que el componente hijo recibe del padre
defineProps({
    edad: String // Propiedad 'edad' de tipo String
});
</script>

<template>
    <!-- Encabezado del componente hijo con estilos en línea -->
    <h6 style="color: blue; font-family:Verdana, Geneva, Tahoma, sans-serif">
        Soy El Componente Hijo 2
        <!-- Icono de carita feliz de Bootstrap -->
        <i class="bi bi-emoji-smile icon"></i>
        <!-- Mostramos el valor de la propiedad 'edad' -->
        <p>{{ edad }}</p>
    </h6>
</template>

<style scoped>
/* Estilos para el icono dentro del componente */
.icon {
    font-size: 20px; /* Tamaño del icono */
    margin-left: 5px; /* Espaciado entre el texto y el icono */
}
</style>
