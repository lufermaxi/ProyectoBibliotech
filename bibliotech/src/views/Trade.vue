<template>
  <div>
    <NavBar />
    <main class="main-section">
      <!--Inicio sección de saludo-->
      <div class="lineTrade-container">
        <h1>Solicitud</h1>
        <h3>de libro en préstamo</h3>
      </div>
      <b-container b-container fluid>
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
        <b-row class="row-books">
          <div class="title-format">
            <h3> Categoría: ILUSTRADO</h3> 
          </div> 
          <b-col cols="12" md="6" lg="2">
            <!--Libro 1-->
            <img v-b-modal.modal-book1 src="../assets/images/illustrated/book-one.png" alt="Los cuentos como son"/>
            <b-modal id="modal-book1" size="lg" centered ok-only hide-footer no-stacking>
              <div class="modal-view1">
                <img class="view-image" src="../assets/images/illustrated/book-one.png" alt="Los cuentos como son"/>
                <p class="info-book">
                  Formato: Ilustración <br />Viaje al centro de la tierra <br />Julio
                  Verne <br />2004 <br />Panamericana Editorial <br />ISBN
                  978-9-58300-688-3 <br /><b>Disponible</b>
                </p>
              </div>
              <div class="btn-solitude">
                <b-button v-b-modal.modal-solitude1>Solicitar</b-button>
              </div>
            </b-modal>
            <b-modal id="modal-solitude1" size="lg" centered ok-only hide-footer>
              <div class="confirmed-box1">
                <img class="view-image" src="../assets/images/illustrated/book-one.png" alt="Los cuentos como son"/>
                <div class="box-check">
                  <p class="confirmed-text">¡Su préstamo ha sido exitoso!</p>
                  <div class ="confirmed-icon">
                    <b-icon icon="check-circle"></b-icon>
                  </div>
                </div>
              </div>
            </b-modal>
          </b-col>
          <b-col cols="12" md="6" lg="2">
            <!--Libro 2-->
            <img v-b-modal.modal-book2 src="../assets/images/illustrated/book-two.png" alt="Harry Potter"/>
            <b-modal id="modal-book2" size="lg" centered ok-only hide-footer no-stacking>
              <div class="modal-view2">
                <img class="view-image" src="../assets/images/illustrated/book-two.png" alt="Harry Potter"/>
                <p class="info-book">
                  Formato: Ilustración <br>Harry Potter: And the goblet of fire
                  <br>J.K. Rowling <br>2016 <br>Pottermore
                  <br>ISBN 978-1-78110-567-2
                  <br><b>Disponible</b>
                </p>
              </div>
              <div class="btn-solitude">
                <b-button v-b-modal.modal-solitude2>Solicitar</b-button>
              </div>
            </b-modal>
            <b-modal id="modal-solitude2" size="lg" centered ok-only hide-footer>
              <div class="confirmed-box2">
                <img class="view-image" src="../assets/images/illustrated/book-two.png" alt="Harry Potter"/>
                <div class="box-check">
                  <p class="confirmed-text">¡Su préstamo ha sido exitoso!</p>
                  <div class ="confirmed-icon">
                    <b-icon icon="check-circle"></b-icon>
                  </div>
                </div>
              </div>
            </b-modal>
          </b-col>
          <b-col cols="12" md="6" lg="2">
            <!--Libro 3-->
            <img v-b-modal.modal-book3 src="../assets/images/illustrated/book-three.png" alt="The squirrels"/>
             <b-modal id="modal-book3" size="lg" centered ok-only hide-footer no-stacking>
              <div class="modal-view3">
                <img class="view-image" src="../assets/images/illustrated/book-three.png" alt="The squirrels"/>
                <p class="info-book">
                  Formato: Ilustración <br>The squirrels who squabbled
                  <br>Rachel Bright, Jim Field <br>2017 <br>Orchard Books
                  <br>ISBN 978-1-40834-048-6
                  <br><b>Disponible</b>
                </p>
              </div>
              <div class="btn-solitude">
                <b-button v-b-modal.modal-solitude3>Solicitar</b-button>
              </div>
            </b-modal>
            <b-modal id="modal-solitude3" size="lg" centered ok-only hide-footer>
              <div class="confirmed-box3">
                <img class="view-image" src="../assets/images/illustrated/book-three.png" alt="The squirrels"/>
                <div class="box-check">
                  <p class="confirmed-text">¡Su préstamo ha sido exitoso!</p>
                  <div class ="confirmed-icon">
                    <b-icon icon="check-circle"></b-icon>
                  </div>
                </div>
              </div>
            </b-modal>
          </b-col>
          <b-col cols="12" md="6" lg="2">
            <!--Libro 4-->
            <img v-b-modal.modal-book4 src="../assets/images/illustrated/book-four.png" alt="Viaje al centro"/>
             <b-modal id="modal-book4" size="lg" centered ok-only hide-footer no-stacking>
              <div class="modal-view4">
                <img class="view-image" src="../assets/images/illustrated/book-four.png" alt="Viaje al centro"/>
                <p class="info-book">
                  Formato: Ilustración <br />Viaje al centro de la tierra <br />Julio
                  Verne <br />2004 <br />Panamericana Editorial <br />ISBN
                  978-9-58300-688-3 <br /><b>Disponible</b>
                </p>
              </div>
              <div class="btn-solitude">
                <b-button v-b-modal.modal-solitude4>Solicitar</b-button>
              </div>
            </b-modal>
            <b-modal id="modal-solitude4" size="lg" centered ok-only hide-footer>
              <div class="confirmed-box4">
                <img class="view-image" src="../assets/images/illustrated/book-four.png" alt="Viaje al centro"/>
                <div class="box-check">
                  <p class="confirmed-text">¡Su préstamo ha sido exitoso!</p>
                  <div class ="confirmed-icon">
                    <b-icon icon="check-circle"></b-icon>
                  </div>
                </div>
              </div>
            </b-modal>
          </b-col>
          <b-col cols="12" md="6" lg="2">
            <!--Libro 5-->
            <img v-b-modal.modal-book5 src="../assets/images/illustrated/book-five.png" alt="Writing the future"/>
             <b-modal id="modal-book5" size="lg" centered ok-only hide-footer no-stacking>
              <div class="modal-view5">
                <img class="view-image" src="../assets/images/illustrated/book-five.png" alt="Writing the future"/>
                <p class="info-book">
                  Formato: Ilustración <br>Writing the Future: <br>Basquiat and the Hip-Hop Generation
                  <br>J. Faith Almiron <br>2020 <br>MFA Publications
                  <br>ISBN 978-0-87846-871-3
                  <br><b>Disponible</b>
                </p>
              </div>
              <div class="btn-solitude">
                <b-button v-b-modal.modal-solitude5>Solicitar</b-button>
              </div>
            </b-modal>
            <b-modal id="modal-solitude5" size="lg" centered ok-only hide-footer>
              <div class="confirmed-box5">
                <img class="view-image" src="../assets/images/illustrated/book-five.png" alt="Writing the future"/>
                <div class="box-check">
                  <p class="confirmed-text">¡Su préstamo ha sido exitoso!</p>
                  <div class ="confirmed-icon">
                    <b-icon icon="check-circle"></b-icon>
                  </div>
                </div>
              </div>
            </b-modal>
          </b-col>
          <b-col cols="12" md="6" lg="2">
            <!--Libro 6-->
            <img v-b-modal.modal-book6 src="../assets/images/illustrated/book-six.png" alt="Batman" />
             <b-modal id="modal-book6" size="lg" centered ok-only hide-footer no-stacking>
              <div class="modal-view6">
                <img class="view-image" src="../assets/images/illustrated/book-six.png" alt="Batman"/>
                <p class="info-book">
                Formato: Ilustración <br>Bataman: Streets of Gotham 
                <br>Paul Dini <br>2011 <br>DC Comics
                <br>ISBN 978-1-40122-722-7 
                <br><b>Disponible</b>
                </p>
              </div>
              <div class="btn-solitude">
                <b-button v-b-modal.modal-solitude6>Solicitar</b-button>
              </div>
            </b-modal>
            <b-modal id="modal-solitude6" size="lg" centered ok-only hide-footer>
              <div class="confirmed-box6">
                <img class="view-image" src="../assets/images/illustrated/book-six.png" alt="Batman"/>
                <div class="box-check">
                  <p class="confirmed-text">¡Su préstamo ha sido exitoso!</p>
                  <div class ="confirmed-icon">
                    <b-icon icon="check-circle"></b-icon>
                  </div>
                </div>
              </div>
            </b-modal>
          </b-col>
        </b-row>
      </b-container>
      <!-- fin libros o articulos que se van a listar-->
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
  data() {
    return {
      books: ["Digital", "Ilustrado", "Manual", "Revista", "Académico"],
    };
  },
};
</script>
