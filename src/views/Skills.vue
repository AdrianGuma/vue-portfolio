<template>
  <div class="container mt-5">

    <h2 class="text-primary-custom fw-bold mb-3">Habilidades Técnicas</h2>

    <div class="row g-4">
      <div class="col-md-6 col-lg-4" v-for="skill in technicalSkills" :key="skill.name">
        <div class="card skill-card p-3 d-flex align-items-center">
          <div class="icon me-3">
            <img :src="skill.icon" alt="" width="40" height="40" />
          </div>
          <div>
            <h5 class="mb-0">{{ skill.name }}</h5>
            <small class="text-muted">{{ skill.level }}</small>
          </div>
        </div>
      </div>
    </div>

    <h2 class="text-primary-custom fw-bold mb-3">Habilidades</h2>

    <div class="d-flex flex-wrap gap-2">
      <span v-for="soft in softSkills" :key="soft" class="badge bg-secondary p-2">{{ soft }}</span>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      technicalSkills: [
        { name: 'HTML', icon: '/icons/html.svg', level: 'Avanzado' },
        { name: 'CSS', icon: '/icons/css.svg', level: 'Avanzado' },
        { name: 'JavaScript', icon: '/icons/js.svg', level: 'Avanzado' },
        { name: 'Vue', icon: '/icons/vue.svg', level: 'Avanzado' },
        { name: 'Laravel', icon: '/icons/laravel.svg', level: 'Intermedio' },
        { name: 'SQL', icon: '/icons/sql.svg', level: 'Intermedio' },
        { name: 'Power Apps', icon: '/icons/powerapps.svg', level: 'Intermedio' },
      ],
      softSkills: ['Trabajo en equipo', 'Manejo de presión', 'Proactividad', 'Compromiso', 'Creatividad']
    }
  }
}
</script>
