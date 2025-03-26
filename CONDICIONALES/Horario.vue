<script>
export default {
  data() {
    return {
      // Definimos la estructura de datos del horario con las materias y docentes correspondientes
      horario: [
        {
          hora: '11:00 - 13:00', // Hora de la clase
          lunes: { materia: 'Redes', docente: 'Abstric' }, // Materia y docente del lunes
          martes: { materia: 'Autonomas', docente: 'Ivor' }, // Martes
          miercoles: { materia: 'Redes', docente: 'Abstric' }, // Miércoles
          jueves: { materia: 'Autonomas', docente: 'Ivor' }, // Jueves
          viernes: { materia: 'Autonomas', docente: 'Ivor' } // Viernes
        },
        {
          hora: '13:00 - 15:00',
          lunes: { materia: 'Software', docente: 'Jose Alfredo' },
          martes: { materia: 'Libre', docente: '' }, // Sin materia asignada
          miercoles: { materia: 'Software', docente: 'Jose Alfredo' },
          jueves: { materia: 'Base de Datos', docente: 'Miguel Angel' },
          viernes: { materia: 'Redes', docente: 'Abstric' }
        },
        {
          hora: '15:00 - 17:00',
          lunes: { materia: 'Programacion Web', docente: 'Josue' },
          martes: { materia: 'Lenguajes de Interfaz', docente: 'Lucia' },
          miercoles: { materia: 'Software', docente: 'Jose Alfredo' },
          jueves: { materia: 'Sistemas Operativos', docente: 'Jorge' },
          viernes: { materia: 'Programacion Web', docente: 'Josue' }
        },
        {
          hora: '17:00 - 19:00',
          lunes: { materia: 'Base de datos', docente: 'Miguel Angel' },
          martes: { materia: 'Lenguajes', docente: 'Lucia' },
          miercoles: { materia: 'Libre', docente: '' },
          jueves: { materia: 'Lenguajes', docente: 'Lucia' },
          viernes: { materia: 'Libre', docente: '' }
        },
      ]
    };
  }
};
</script>

<template>
  <div class="horario-container"> <!-- Contenedor principal del horario -->
    <h1 class="titulo-horario">Horario Estudiantil</h1> <!-- Título principal -->

    <div class="tabla-container"> <!-- Contenedor para la tabla -->
      <table class="tabla-horario"> <!-- Tabla del horario -->
        <thead>
          <tr> <!-- Fila de encabezado -->
            <th>Hora</th> <!-- Encabezado para las horas -->
            <th>Lunes</th> <!-- Encabezado para lunes -->
            <th>Martes</th> <!-- Encabezado para martes -->
            <th>Miércoles</th> <!-- Encabezado para miércoles -->
            <th>Jueves</th> <!-- Encabezado para jueves -->
            <th>Viernes</th> <!-- Encabezado para viernes -->
          </tr>
        </thead>
        <tbody>
          <!-- Iteramos sobre el array de "horario" para generar las filas de la tabla -->
          <tr v-for="(clase, index) in horario" :key="index">
            <td>{{ clase.hora }}</td> <!-- Muestra la hora en la primera columna -->
            <!-- Cada celda muestra la materia en negrita y el docente en cursiva -->
            <td>
              <strong>{{ clase.lunes.materia }}</strong> <!-- Nombre de la materia -->
              <br>
              <span class="docente">{{ clase.lunes.docente }}</span> <!-- Nombre del docente -->
            </td>
            <td>
              <strong>{{ clase.martes.materia }}</strong>
              <br>
              <span class="docente">{{ clase.martes.docente }}</span>
            </td>
            <td>
              <strong>{{ clase.miercoles.materia }}</strong>
              <br>
              <span class="docente">{{ clase.miercoles.docente }}</span>
            </td>
            <td>
              <strong>{{ clase.jueves.materia }}</strong>
              <br>
              <span class="docente">{{ clase.jueves.docente }}</span>
            </td>
            <td>
              <strong>{{ clase.viernes.materia }}</strong>
              <br>
              <span class="docente">{{ clase.viernes.docente }}</span>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<style scoped>
/* Estilos generales del contenedor del horario */
.horario-container {
  max-width: 1200px;
  margin: 2rem auto;
  padding: 2rem;
  background: #f9f9f9; /* Color de fondo */
  border-radius: 15px; /* Bordes redondeados */
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1); /* Sombra sutil */
}

/* Estilos del título */
.titulo-horario {
  color: #0056b3;
  text-align: center;
  font-size: 2rem;
}

/* Contenedor de la tabla para hacerla responsiva */
.tabla-container {
  margin-top: 2rem;
  overflow-x: auto;
}

/* Estilos generales de la tabla */
.tabla-horario {
  width: 100%;
  border-collapse: collapse; /* Une los bordes de las celdas */
  margin-top: 1rem;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.05);
  border-radius: 10px;
}

/* Estilos para los encabezados de la tabla */
.tabla-horario th {
  background-color: #0056b3; /* Azul oscuro */
  color: white;
  font-weight: bold;
  padding: 1rem;
  text-align: center;
}

/* Estilos de las celdas de la tabla */
.tabla-horario td {
  padding: 1rem;
  text-align: center;
  border: 1px solid #e0e0e0; /* Bordes grises */
}

/* Estilos para filas alternas de la tabla */
.tabla-horario tr:nth-child(even) {
  background-color: #f1f1f1; /* Color gris claro */
}

/* Efecto hover para resaltar filas */
.tabla-horario tr:hover {
  background-color: #e0f7ff; /* Azul muy claro */
}

/* Estilos para el nombre del docente */
.docente {
  font-size: 0.9rem; /* Tamaño más pequeño */
  color: #555; /* Color gris oscuro */
  font-style: italic; /* Texto en cursiva */
}
</style>
