<template>
  <div>
    <NavBar />
    <main>
      <!--Inicio de la página de acerca de-->
      <section id="trade" class="trade-section">
        <div class="lineTrade-container">
          <h1>Acerca de</h1>
          <h3>Conoce a Bibliotech</h3>
        </div>
      </section>
      <!--informacion y noticias de la empresa-->
      <section class="wrapper-main">
        <div class="row1-news">
          <div class="bibliotech-news">
            <img
              class="photo-one"
              src="../assets/images/library.png"
              alt="Una librería"
            />
            <a class="btn-about" href="#">Conoce más</a>
            <!--Se plantea este conoce más dirigirlo a un video (en youtube puede ser) que explique qué es Bibliotech, SI ALCANZAMOS-->
          </div>
          <div class="info-news">
            <p>
              <b>Bibliotech</b> es un sistema de gestión <br />
              de libros dirigido a los servicios bibliotecarios <br />
              y a sus usuarios que aman los libros
            </p>
          </div>
        </div>
        <div class="row2-news">
          <div class="news1-news">
            <img
              class="photo-two"
              src="../assets/images/books.png"
              alt="Pila de libros"
            />
            <a class="headline-news1" href="#wrap-modal1"
              >¿Cómo Bibliotech<br />
              hizo de nuevo una tendencia los libros?<br />+</a
            >
          </div>
          <div class="news2-news">
            <img
              class="photo-three"
              src="../assets/images/programmin-book.png"
              alt="Libro de programación"
            />
            <a class="headline-news2" href="#wrap-modal2"
              >Alianza TIC<br />
              para el aprendizaje de programación mediante libros<br />+</a
            >
          </div>
        </div>
        <!--Ventana modal de noticias-->
        <div id="wrap-modal1" class="modal-n">
          <div class="modal-news1">
            <h1 class="title-news">
              ¿Cómo Bibliotech hizo de nuevo una tendencia los libros?
            </h1>
            <p class="text-news">
              Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eum
              fugiat facilis recusandae saepe vel eveniet distinctio quae nulla
              cupiditate consectetur totam est optio impedit laborum, sunt ab
              placeat sint nesciunt. Lorem, ipsum dolor sit amet consectetur
              adipisicing elit. Eum fugiat facilis recusandae saepe vel eveniet
              distinctio quae nulla cupiditate consectetur totam est optio
              impedit laborum, sunt ab placeat sint nesciunt.
            </p>
            <div class="news-btn">
              <a href="#">Regresar</a>
            </div>
          </div>
        </div>

        <div id="wrap-modal2" class="modal-n">
          <div class="modal-news2">
            <h1 class="title-news">
              Alianza TIC para el aprendizaje de programación mediante libros
            </h1>
            <p class="text-news">
              Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eum
              fugiat facilis recusandae saepe vel eveniet distinctio quae nulla
              cupiditate consectetur totam est optio impedit laborum, sunt ab
              placeat sint nesciunt. Lorem, ipsum dolor sit amet consectetur
              adipisicing elit. Eum fugiat facilis recusandae saepe vel eveniet
              distinctio quae nulla cupiditate consectetur totam est optio
              impedit laborum, sunt ab placeat sint nesciunt.
            </p>
            <div class="news-btn">
              <a href="#">Regresar</a>
            </div>
          </div>
        </div>
      </section>
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
