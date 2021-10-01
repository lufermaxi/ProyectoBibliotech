<template>
  <div>
    <header id="index" class="header-section">
      <!--Inicio con logo de Bibliotech-->
      <div class="logo">
        <router-link to="/">
          <img src="../assets/images/logo-micro.png" alt="Logo de bibliotech" />
        </router-link>
      </div>
      <!--Barra de navegación-->
      <div class="bar">
        <div class="nav-bar">
          <router-link to="Trade">Préstamo</router-link>
          <router-link to="About">Acerca de</router-link>
          <router-link to="Team">Equipo</router-link>
        </div>
        <div class="login-bar">
          <router-link to="Login">Log In</router-link>
        </div>
      </div>
    </header>
  </div>
</template>
