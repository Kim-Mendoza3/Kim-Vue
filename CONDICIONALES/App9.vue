<script>
export default {
  data() {
    return {
      alumnos: [
        { nc: 22730001, nombre: 'Emiliano Rivas Castro', carrera: 'Arquitectura', gusto: 'Fotografía' },
        { nc: 22730002, nombre: 'Camila Ortega Valdés', carrera: 'Medicina', gusto: 'Cine y documentales' },
        { nc: 22730003, nombre: 'Diego Herrera Ruiz', carrera: 'Ingeniería Civil', gusto: 'Escalar montañas' },
        { nc: 22730004, nombre: 'Valentina Pérez Gómez', carrera: 'Psicología', gusto: 'Pintar y dibujar' },
        { nc: 22730005, nombre: 'Javier Martínez López', carrera: 'Administración', gusto: 'Tocar la guitarra' },
        { nc: 22730006, nombre: 'Isabela Torres Sánchez', carrera: 'Derecho', gusto: 'Aprender idiomas' }
      ]
    };
  },
  computed: {
    filteredAlumnos() {
      return this.alumnos;
    }
  }
};
</script>

<template>
  <div class="container">
    <h1 class="titulo">Lista de Estudiantes</h1>
    <p class="info">Profesor: Josue Israel Vazquez Martinez</p>
    <p class="info">Materia: Programación Web</p>
    <p class="info">Grupo: 6AS</p>
    
    <div class="table-responsive">
      <table class="tabla">
        <thead>
          <tr>
            <th>No. Control</th>
            <th>Nombre</th>
            <th>Carrera</th>
            <th>Gusto</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="alumno in filteredAlumnos" :key="alumno.nc">
            <td>{{ alumno.nc }}</td>
            <td>{{ alumno.nombre }}</td>
            <td>{{ alumno.carrera }}</td>
            <td>{{ alumno.gusto }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<style scoped>
body {
  background: linear-gradient(135deg, #ff9a9e, #fad0c4);
  font-family: 'Poppins', sans-serif;
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}

.container {
  max-width: 1200px;
  padding: 2rem;
  background: white;
  border-radius: 15px;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
  text-align: center;
}

.titulo {
  color: #333;
  font-size: 2rem;
  font-weight: 600;
}

.info {
  color: #555;
  font-size: 1.2rem;
  margin: 5px 0;
}

.table-responsive {
  overflow-x: auto;
}

.tabla {
  width: 100%;
  border-collapse: collapse;
  margin-top: 1rem;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  border-radius: 10px;
}

.tabla th, 
.tabla td {
  padding: 1.5rem;
  text-align: center;
  border: 1px solid #f0f0f0;
  font-size: 1.1rem;
}

.tabla th {
  background-color: #ff758c;
  color: white;
  font-weight: bold;
}

.tabla tr:nth-child(even) {
  background-color: #ffe2e2;
}

.tabla tr:hover {
  background-color: #ffccd5;
  transition: 0.3s;
}
</style>
