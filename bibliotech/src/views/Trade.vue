<template>
  <div>
    <NavBar />
    <main class="main-section">
      <!--Inicio sección de saludo-->
      <div class="lineTrade-container">
        <h1>Solicitud</h1>
        <h3>de libro en préstamo</h3>
      </div>
      <b-container fluid>
        <div class="box-search">
          <div class="search-text">
            <label for="search-book">Búsqueda de artículos</label>
          </div>
          <div class="box">
            <b-form-input list="search-list" id="search-book"></b-form-input>
            <b-form-datalist id="search-list" :options="books"></b-form-datalist>
          </div>
          <div class="button">
            <b-button @click="books">Buscar</b-button>
          </div>
        </div>
        <ListBooks />
      </b-container>
      <!-- fin libros o articulos que se van a listar-->
    </main>
    <Footer />
  </div>
</template>
<script>
import NavBar from "../components/navbar.vue";
import Footer from "../components/footer.vue";
import ListBooks from "../components/listBooks.vue";
export default {
  components: {
    NavBar,
    Footer,
    ListBooks,
  },
  data() { //Lista búsqueda de categorias de libros disponibles
    return {
      books: ["Digital", "Ilustración", "Manual", "Revista", "Académico"],
    };
  },
};
</script>
<style scoped>
.form-control{
    border: 1px solid #ff3000 !important;
}
.btn-secondary{
    background-color: #485eb2 !important;
    border: 1px solid #485eb2 !important;
}
</style>