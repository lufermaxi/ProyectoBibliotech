<template>
  <div>
    <b-container fluid>
      <b-row class="footer-row">
        <!--Clase para diseño de colores: azul-->
        <b-col cols="12"  class="blue-1" >
          <!--Columna de diseño-->
          <b-col class="logo-foot" sm="12" lg="3">
            <img src="../assets/images/white-logo.png" alt="Logo del footer" />
          </b-col>
          <b-col class="info-foot" sm="12" lg="3">
            <!--Info de creación-->
            <h2>Contáctanos:</h2>
            <h3>© Bibliotech 2021</h3>
            <h3>--Todos los derechos reservados--</h3>
            <h3>Cookies & privacy policy</h3>
          </b-col>
          <b-col class="icons-foot" sm="12" lg="3">
            <!--Lista de íconos-->
            <a href="https://github.com/afar-cmyk/ProyectoBibliotech">
              <h6>Bibliotech</h6>
              <b-icon class="git-icon" icon="github"></b-icon>
            </a>
            <a href="https://web.telegram.org/z/#-540770927">
              <h6>Grupo 1/21</h6>
              <b-icon class="tel-icon" icon="telephone"></b-icon>
            </a>
          </b-col>
          <b-col class="nav-foot" sm="12" lg="3">
            <!--Lista de navegación de footer-->
            <ul>
              <li><router-link to="/">Inicio</router-link></li>
              <li><router-link to="Trade">Préstamo</router-link></li>
              <li><router-link to="About">Acerca de</router-link></li>
              <li><router-link to="Team">Equipo</router-link></li>
              <li><router-link to="Login">Log In</router-link></li>
            </ul>
          </b-col>
        </b-col>
      </b-row>
      <b-row>
        <b-col class="orange-2" cols="4"><br /></b-col>
        <b-col class="orange-3" cols="4"><br /></b-col>
        <b-col class="orange-4" cols="4"><br /></b-col>
      </b-row>
    </b-container>
  </div>
</template>
