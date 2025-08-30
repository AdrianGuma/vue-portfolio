<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-dark">
      <div class="container">
        <a class="navbar-brand fs-4" href="#">Adrián Guzmán</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav ms-auto">
            <li class="nav-item"><router-link class="nav-link" to="/">Home</router-link></li>
            <li class="nav-item"><router-link class="nav-link" to="/about">Sobre mí</router-link></li>
            <li class="nav-item"><router-link class="nav-link" to="/skills">Habilidades</router-link></li>
            <li class="nav-item"><router-link class="nav-link" to="/experience">Experiencia</router-link></li>
            <li class="nav-item"><router-link class="nav-link" to="/contact">Contacto</router-link></li>
          </ul>
        </div>
      </div>
    </nav>

    <router-view />
  </div>
</template>

<script>
export default {
  name: 'App',
}
</script>

<style>
/* Puedes poner estilos globales aquí si quieres */
</style>