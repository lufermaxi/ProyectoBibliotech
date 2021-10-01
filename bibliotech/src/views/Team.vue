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
      <section class="wrapper-main">
        <div class="info-team">
          <div class="team-one">
            <div class="ph">
              <img src="../assets/images/ex-photo-man.jpg" alt="Foto Andrés">
            </div>
            <h3 class="name">
              Andrés Felipe Álvarez &nbsp;
            </h3>
            <p class="info">
              Tecnólogo en producción de Multimedia, apasionado por la fotografía y el diseño
            </p>
            <h4 class="occupation">
              Creative leader
            </h4>
            <h4 class="occupation">
              Scrum: Product owner, Developer team
            </h4>
            <div class="contact-team">
              <p>Conoce más</p>
              <a href="">+</a>
            </div>
          </div>
          <div class="team-two">
            <div class="ph">
              <img src="../assets/images/ex-photo-man.jpg" alt="Foto Esteban">
            </div>
            <h3 class="name">
              Juan Esteban Castiblanco
            </h3>
            <p class="info">
              Estudiante de economía e Ingeniería estadística
            </p>
            <h4 class="occupation">
              Sales Manager
            </h4>
            <h4 class="occupation">
              Scrum: Developer team
            </h4>
            <div class="contact-team">
              <p>Conoce más</p>
              <a href="">+</a>
            </div>
          </div>
          <div class="team-three">
            <div class="ph">
              <img src="../assets/images/ex-photo-woman.jpg" alt="Foto Kelly">
            </div>
            <h3 class="name">
              Kelly Monroy Carrillo &nbsp;&nbsp;
            </h3>
            <p class="info">
              Diseñadora digital y multimedia, ilustradora y artista
            </p>
            <h4 class="occupation">
              Web designer
            </h4>
            <h4 class="occupation">
              Scrum: Developer team
            </h4>
            <div class="contact-team">
              <p>Conoce más</p>
              <a href="">+</a>
            </div>
          </div>
          <div class="team-four">
            <div class="ph">
              <img src="../assets/images/ex-photo-man.jpg" alt="Foto John">
            </div>
            <h3 class="name">
              John Stiven Vásquez &nbsp;&nbsp;
            </h3>
            <p class="info">
              Estudiante universitario interesado en la programación y con experiencia en Java
            </p>
            <h4 class="occupation">
              Web developer
            </h4>
            <h4 class="occupation">
              Scrum: Scrum master, developer team
            </h4>          
            <div class="contact-team">
              <p>Conoce más</p>
              <a href="">+</a>
            </div>
          </div>
          <div class="team-five">
            <div class="ph">
              <img src="../assets/images/ex-photo-man.jpg" alt="Foto Luis">
            </div>
            <h3 class="name">
              Luis Fernando Delgado
            </h3>
            <p class="info">
              Estudiante...
            </p>
            <h4 class="occupation">
              Web developer
            </h4>
            <h4 class="occupation">
              Scrum: Product owner, developer team
            </h4>
            <div class="contact-team">
              <p>Conoce más</p>
              <a href="">+</a>
            </div>
          </div>
        </div>
      </section>
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
