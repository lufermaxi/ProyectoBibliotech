<template>
  <div>
    <NavBar />
    <main class="main-section">
      <!--Inicio de contenido de la página index-->
      <b-row class="line-container">
        <b-col>
          <h1>¡Bienvenido!</h1>
          <h3>a nuestro sistema bibliotecario</h3>
        </b-col>
      </b-row>
      |
      <b-container class="wrapper-main" fluid>
        <!--Sección para imagen central de los libros de Bibliotech-->
        <b-row>
          <b-col cols="12" md="6" class="banner-image">
            <img src="../assets/images/index-image.png" alt="Banner de inicio"/>
          </b-col>
        </b-row>
        <!--Saludo e invitación a ir a préstamo-->
        <div class="banner-text">
          <h3>¡Hola!</h3>
          <h5>¿Necesita un libro?</h5>
          <div class="button-solitude">
            <router-link to="Trade">Préstamo</router-link>
          </div>
        </div>
      </b-container>
    </main>
    <Footer />
  </div>
</template>
<script>
import NavBar from "../components/navbar.vue";
import Footer from "../components/footer.vue";

export default {
  components: {
    NavBar,
    Footer,
  },
};
</script>
