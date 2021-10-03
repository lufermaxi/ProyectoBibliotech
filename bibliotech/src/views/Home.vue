<template>
  <div>
    <NavBar />
    <main class="main-section">
      <!--Inicio de contenido de la página index-->
      <div class="line-container">
          <h1>¡Bienvenido!</h1>
          <h3>a nuestro sistema bibliotecario</h3>
      </div>
      <b-container fluid>
        <!--Sección para imagen central de los libros de Bibliotech-->
        <b-row class="banner-image">
          <b-col cols="12" md="12" lg="6">
            <img class="banner-image1" src="../assets/images/index-image1.png" fluid alt="Banner de inicio"/>
          </b-col>
          <b-col cols="12" md="12" lg="6">
            <img class="banner-image2" src="../assets/images/index-image2.png" fluid alt="Banner de inicio"/>
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
