<template>
  <div class="container mt-5">

    <h2 class="text-primary-custom fw-bold mb-3">Experiencia y Proyectos</h2>

    <div class="row g-4">
      <div class="col-md-6" v-for="project in projects" :key="project.title">
        <div class="card p-4">
          <h5 class="fw-bold">{{ project.title }}</h5>
          <p class="text-gray-300">{{ project.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        { title: 'Portafolio web', description: 'Desarrollo de portafolios web en Vue y Bootstrap.' },
        { title: 'Sistema POS para restaurante', description: 'Creación de un sistema de punto de venta con roles de mesero, cajero y administrador.' },
        { title: 'Cortometrajes', description: 'Proyectos de cortometraje con enfoque creativo y social.' },
        { title: 'Desarrollo de soluciones digitales personalizadas', description: 'Implementación de sistemas interactivos para empresas, con dashboards, formularios y gestión de datos.' }
      ]
    }
  }
}
</script>
