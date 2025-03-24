<script>
export default {
  data() {
    return {
      horario: [
        {
          hora: '11:00 - 13:00',
          lunes: { materia: 'Redes', docente: 'Abstric' },
          martes: { materia: 'Autonomas', docente: 'Ivor' },
          miercoles: { materia: 'Redes', docente: 'Abstric' },
          jueves: { materia: 'Autonomas', docente: 'Ivor' },
          viernes: { materia: 'Autonomas', docente: 'Ivor' }
        },
        {
          hora: '13:00 - 15:00',
          lunes: { materia: 'Software', docente: 'Jose Alfredo' },
          martes: { materia: 'Libre', docente: '' },
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
  <div class="horario-container">
    <h1 class="titulo-horario">Horario Estudiantil</h1>
    
    <div class="tabla-container">
      <table class="tabla-horario">
        <thead>
          <tr>
            <th>Hora</th>
            <th>Lunes</th>
            <th>Martes</th>
            <th>Miércoles</th>
            <th>Jueves</th>
            <th>Viernes</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(clase, index) in horario" :key="index">
            <td>{{ clase.hora }}</td>
            <td>
              <strong>{{ clase.lunes.materia }}</strong>
              <br>
              <span class="docente">{{ clase.lunes.docente }}</span>
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
.horario-container {
  max-width: 1200px;
  margin: 2rem auto;
  padding: 2rem;
  background: #f9f9f9;
  border-radius: 15px;
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
}

.titulo-horario {
  color: #0056b3;
  text-align: center;
  font-size: 2rem;
}

.tabla-container {
  margin-top: 2rem;
  overflow-x: auto;
}

.tabla-horario {
  width: 100%;
  border-collapse: collapse;
  margin-top: 1rem;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.05);
  border-radius: 10px;
}

.tabla-horario th {
  background-color: #0056b3;
  color: white;
  font-weight: bold;
  padding: 1rem;
  text-align: center;
}

.tabla-horario td {
  padding: 1rem;
  text-align: center;
  border: 1px solid #e0e0e0;
}

.tabla-horario tr:nth-child(even) {
  background-color: #f1f1f1;
}

.tabla-horario tr:hover {
  background-color: #e0f7ff;
}

.docente {
  font-size: 0.9rem;
  color: #555;
  font-style: italic;
}
</style>
