<template>
  <div>
    <NavBar />
     <main class="main-section">
       <!--Inicio de contenido de la página team-->
       <div class="line-container">
        <h1>Equipo</h1>
        <h3>Conozca a nuestro equipo</h3>
      </div>
      <!--Inicio contenido información de las personas del equipo-->
      <b-container fluid>
        <b-row class="row-team">
          <b-col cols="12" md="12" lg="3">
            <b-card>
              <div class="team-one">
                <b-img :src="require('../assets/images/ex-photo-man.jpg')" />
                <b-text>
                  <h4 class="name">Andrés Felipe Álvarez</h4>
                  <p class="info">Tecnólogo en producción de Multimedia, apasionado por la fotografía y el diseño</p>
                  <h5 class="occupation">Desarrollador backend y frontend, diseñador web</h5>
                  <b-button class="contact-team">Contacto</b-button>
                </b-text>
              </div>
            </b-card>
          </b-col>
          <b-col cols="12" md="12" lg="2" class="team-two">
             <b-card>
              <div class="team-two">
                <b-img :src="require('../assets/images/ex-photo-man.jpg')" />
                <b-text>
                  <h4 class="name">Juan Esteban Castiblanco</h4>
                  <p class="info">Estudiante de economía e Ingeniería estadística</p>
                  <h5 class="occupation">Desarrollador backend</h5>
                  <b-button class="contact-team">Contacto</b-button>
                </b-text>
              </div>
            </b-card>
          </b-col>
          <b-col cols="12" md="12" lg="2">
             <b-card>
              <div class="team-three">
                <b-img :src="require('../assets/images/ex-photo-woman.jpg')" />
                <b-text>
                  <h4 class="name">Kelly Monroy Carrillo</h4>
                  <p class="info">Diseñadora digital y multimedia, ilustradora y artista</p>
                  <h5 class="occupation">Diseñadora web y desarrolladora frontend</h5>
                  <b-button class="contact-team">Contacto</b-button>
                </b-text>
              </div>
            </b-card>
          </b-col>
          <b-col cols="12" md="12" lg="2">
             <b-card>
              <div class="team-four">
                <b-img :src="require('../assets/images/ex-photo-man.jpg')" />
                <b-text>
                  <h4 class="name">John Stiven Vásquez</h4>
                  <p class="info">Estudiante universitario interesado en la programación y con experiencia en Java</p>
                  <h5 class="occupation">Desarrollador backend, bases de datos</h5>
                  <b-button class="contact-team">Contacto</b-button>
                </b-text>
              </div>
            </b-card>
          </b-col>
          <b-col cols="12" md="12" lg="3">
             <b-card>
              <div class="team-five">
                <b-img :src="require('../assets/images/ex-photo-man.jpg')" />
                <b-text>
                  <h4 class="name">Luis Fernando Delgado</h4>
                  <p class="info">Estudiante de programación con habilidad en el manejo de sistemas: hardware y software</p>
                  <h5 class="occupation">Desarrollador backend y web</h5>
                  <b-button class="contact-team">Contacto</b-button>
                </b-text>
              </div>
            </b-card>
          </b-col>
        </b-row>
      </b-container>
    <!--Fin contenido del equipo-->
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
<style>
.btn-secondary{
    background-color: #485eb2 !important;
    border: 1px solid #485eb2 !important;
}
</style>
