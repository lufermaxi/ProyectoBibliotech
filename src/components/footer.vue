<template>
  <div>
    <b-container fluid>
      <b-row cols="4">
        <b-col cols="9" class="blue-1">
          <b-row>
            <b-col cols="12" md="6" lg="3" class="logo-foot">
              <img src="../assets/images/white-logo.png" fluid alt="Logo del footer" />
            </b-col>
            <b-col cols="12" md="6" lg="3" class="info-foot">
               <!--Info de creación-->
              <h3>© Bibliotech 2021</h3>
              <h3>--Todos los derechos reservados--</h3>
              <h3>Cookies & privacy policy</h3>
            </b-col>
            <b-col cols="12" md="6" lg="3" class="icons-foot">
               <!--Lista de íconos-->
              <h2 class="contact">Contáctanos:</h2>
              <a href="https://github.com/afar-cmyk/ProyectoBibliotech">
                <b-icon class="git-icon" icon="github"></b-icon>
              </a>
              <a href="https://web.telegram.org/z/#-540770927">
                <b-icon class="tel-icon" icon="telephone"></b-icon>
              </a>
            </b-col>
            <b-col cols="12" md="6" lg="3" class="nav-foot">
              <!--Lista de navegación de footer-->
              <ul>
                <li><router-link to="/">Inicio</router-link></li>
                <li><router-link to="Trade">Préstamo</router-link></li>
                <li><router-link to="About">Acerca de</router-link></li>
                <li><router-link to="Team">Equipo</router-link></li>
                <li><router-link to="Login">Log In</router-link></li>
              </ul>
            </b-col>
          </b-row>
        </b-col>
        <b-col cols="1" class="orange-2"></b-col>
        <b-col cols="1" class="orange-3"></b-col>
        <b-col cols="1" class="orange-4"></b-col>
      </b-row>

    </b-container>
    
  </div>
</template>