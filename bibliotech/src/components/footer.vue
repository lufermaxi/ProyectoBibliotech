<template>
  <div>
    <footer class="footer-section">
      <!--Inicio del contenido del footer-->
      <div class="blue-1">
        <!--Clase para diseño de colores: azul-->
        <div class="logo-foot">
          <img src="../assets/images/white-logo.png" alt="Logo del footer" />
        </div>
        <!--Info de creación-->
        <div class="info-foot">
          <h2>Contáctanos:</h2>
          <h3>© Bibliotech 2021</h3>
          <h3>-Todos los derechos reservados-</h3>
          <h3>Cookies & policy privacy</h3>
        </div>
        <!--Lista de íconos-->
        <div class="icons-foot">
          <ul>
            <li>
              <a href="https://github.com/afar-cmyk/ProyectoBibliotech"
                >Github</a
              >
            </li>
            <li>
              <a href="https://web.telegram.org/z/#-540770927">Telegram</a>
            </li>
          </ul>
        </div>
        <!--Lista de navegación de footer-->
        <div class="nav-foot">
          <ul>
            <li><router-link to="/">Inicio</router-link></li>
            <li><router-link to="Trade">Préstamo</router-link></li>
            <li><router-link to="About">Acerca de</router-link></li>
            <li><router-link to="Team">Equipo</router-link></li>
            <li><router-link to="Login">Log In</router-link></li>
          </ul>
        </div>
      </div>
      <!--Clases para diseño de colores de fondo de footer: naranjas-->
      <div class="orange-2"></div>
      <div class="orange-3"></div>
      <div class="orange-4"></div>
    </footer>
  </div>
</template>
