<template>
  <div>
    <NavBar />
    <main class="main-section">
      <!--Inicio de contenido de la página index-->
      <div class="line-container">
        <h1>¡Bienvenido!</h1>
        <h3>a nuestro sistema bibliotecario</h3>
      </div>
      <!--Sección para imagen central de los libros de Bibliotech-->
      <section class="wrapper-main">
        <div class="banner-image">
          <img src="../assets/images/index-image.png" alt="Banner de inicio" />
        </div>
        <!--Saludo e invitación a ir a préstamo-->
        <div class="banner-text">
          <h3>¡Hola!</h3>
          <h5>¿Necesita un libro?</h5>
          <div class="button-solitude">
            <router-link to="Trade">Préstamo</router-link>
          </div>
        </div>
      </section>
      <!---Fin del contenido de la página index-->
    </main>
    <Footer />
  </div>
</template>
<script>
import NavBar from '../components/navbar.vue'
import Footer from '../components/footer.vue'

export default {
  components: {
    NavBar,
    Footer,
  },
};
</script>
