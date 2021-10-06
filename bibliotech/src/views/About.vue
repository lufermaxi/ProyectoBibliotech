<template>
  <div>
    <NavBar />
    <main>
      <div class="line-container">
        <h1>Acerca de</h1>
        <h3>Conoce a Bibliotech</h3>
      </div>
      <!--informacion y noticias de la empresa-->
      <b-container fluid class="rows-news">
        <b-row class="row-news1">
          <!--Noticia 1-->
          <b-col cols="12" md="6" lg="6">
            <!--Se añade require porque no lee este tipo de componente de Bootstrap-->
            <b-card class="news1-bibliotech" overlay :img-src="require('../assets/images/library.png')" img-alt="Una Biblioteca">
              <b-button v-b-modal.modal-news3 class="btn-plus">Conoce +</b-button>
              <!--Dirige a una presentación-->
            </b-card>
          </b-col>
          <!--Noticia 2-->
          <b-col cols="12" md="6" lg="6">
            <b-card class="news2-text"> 
              <b-card-text>
                <p><b>Bibliotech</b> es un sistema de gestión
                  de libros dirigido a los servicios bibliotecarios
                  y a sus usuarios que aman los libros</p>
              </b-card-text>
            </b-card>
          </b-col>
        </b-row>
        <b-row class="row-news2">
          <!--Noticia 3-->
          <b-col cols="12" md="6" lg="6"> 
            <b-card v-b-modal.modal-news3 class="news3-how" overlay :img-src="require('../assets/images/books.png')" img-alt="Libros">
              <b-card-text> 
                <p>¿Cómo Bibliotech logró que los libros sean de nuevo una tendencia?</p>
              </b-card-text> 
            </b-card>
          </b-col>
          <b-modal id="modal-news3" size="lg" centered ok-only hide-footer>
            <h3 class="title-modal">
              ¿Cómo Bibliotech logró que los libros sean de nuevo una tendencia?
            </h3>
            <p class="text-modal">
              La implementación de Bibliotech como gestor de bibliotecas en diversas empresas,
              ha generado un interés de los participantes, por los libros; las solicitudes
              han aumentado desde su inicio a finales de septiembre de 2021, la gente quiere leer 
              y este sistema ha permitido el acceso a una gran colección de ejemplares que pueden obtener
              de una manera sencilla y gratuita.<br />
              Además, el sitio brinda ejemplares de enseñanza en ciencia y tecnología que abren paso al aprendizaje
              en estas áreas, los libros acercan a la tecnología y la tecnología le da un nuevo valor a los libros.<br /><br />
              Por: <i>Redacción Bibliotech</i>
            </p>
          </b-modal>
          <!--Noticia 4-->
          <b-col cols="12" md="6" lg="6">
            <b-card v-b-modal.modal-news4 class="news4-prog" overlay :img-src="require('../assets/images/programmin-book.png')" img-alt="Libros de programación">
              <b-card-text>
                <p>Alianza TIC para el aprendizaje en programación con libros</p>
              </b-card-text>
            </b-card>
          </b-col>
          <b-modal id="modal-news4" size="lg" centered ok-only hide-footer>
            <h3 class="title-modal">
              Alianza TIC para el aprendizaje en programación con libros
            </h3>
            <p class="text-modal">
              Bibliotech sigue acercando a la tecnología, el pasado 1 de octubre la alianza entre el gestor de bibliotecas y el
              ministerio TIC ha abierto un camino de enseñanza por medio de libros, e-books, manuales y revistas de programación, la idea 
              es acercar a todo público al proceso de aprendizaje de múltiples lenguajes de programación, desarrollo web y 
              desarrollo movil. <br />
              "Creemos que el aprendizaje debe ir más allá de la tecnología por eso los libros y manuales son imprescindibles
              en la enseñanza de programación y desarrollo, la llamada brecha digital se cierra con un buen nivel de práctica y teoría, por eso 
              nos alegra ser parte de este proceso" dijo el equipo creador de Bibliotech. <br /><br />
              Por: <i>Redacción Bibliotech</i>
            </p>
          </b-modal>
        </b-row>
      </b-container>
    </main>
    <Footer/>
  </div>
</template>
<script>
import NavBar from '../components/navbar.vue'
import Footer from '../components/footer.vue'

export default {
  components: {
    NavBar,
    Footer
  }
}
</script>
<style scoped>
.rows-news{
    background-color: #f3f3f3 !important;
}
.row-news1{
    margin-top: 4rem !important;
    padding: 1rem;
}
.news1-bibliotech{
    border: none !important;
}
.news3-how{
    margin-top: 3rem;
    border: none !important;
}
.news4-prog{
    margin-top: 3rem;
    border: none !important;
}
.card{
    background-color: #f3f3f3 !important;
}
.news2-text{
    border: none !important;
}
.btn-secondary{
    background-color: #485eb2 !important;
    border: 1px solid #485eb2 !important;
}
</style>
