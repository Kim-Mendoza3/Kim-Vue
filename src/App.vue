<script setup lang="ts">
import App9 from '../CONDICIONALES/App9.vue';
// Importamos el componente "Horario" desde la carpeta "CONDICIONALES"
// Esto permite utilizar el componente en este archivo.
// import Horario from '../CONDICIONALES/Horario.vue';
// import PADRE from './components/PROPS/PADRE.vue';
// import HIJO1 from './components/PROPS/HIJO1.vue';
//  import HIJO2 from './components/PROPS/HIJO2.vue';
// import EVENTOS from './components/EVENTOS/EVENTOS.vue';
import Calculadora from './components/CALCULADORA/Calculadora.vue';

// import AppCard from './components/AppCard.vue';
// import Card from './components/AppCard.vue';
// import Equipo from './components/equipo.vue';

</script>

<template>
  <!-- <h1>Pioli & Silvestre </h1> -->
  <div class="container d-flex flex-column align-items-center vh-100">
    <div class="row" >

    </div>
    <!-- <AppCard/> -->
    <!-- <AppCard/> -->
    <!-- <Equipo/> -->
     <!-- <App9/>  -->
      <!-- <Horario/>     Se llama al componente "Horario", que se mostrará en la interfaz -->
       <!-- <PADRE/> Se llama al componente "Horario", que se mostrará en la interfaz  -->
    <!-- <EVENTOS/> -->
     <Calculadora/>



  </div>
</template>



<style>
/* Estilos adicionales si es necesario */
</style>