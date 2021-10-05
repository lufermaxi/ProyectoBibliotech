<template>
  <div>
    <b-navbar toggleable="md" class="header">
      <!--Inicio con logo de Bibliotech-->
      <b-navbar-brand class="logo">
        <router-link to="/">
          <img src="../assets/images/logo-micro.png" alt="Logo de bibliotech" />
        </router-link>
      </b-navbar-brand>

      <b-navbar-toggle target="navbar-toggle-collapse">
        <template #default="{ expanded }">
          <b-icon v-if="expanded" icon="x"></b-icon>
          <b-icon v-else icon="list"></b-icon>
        </template>
      </b-navbar-toggle>

      <b-collapse id="navbar-toggle-collapse" is-nav>
        <b-navbar-nav class="nav-bar">
          <router-link to="Trade">Préstamo</router-link>
          <router-link to="About">Acerca de</router-link>
          <router-link to="Team">Equipo</router-link>
          <div class="login-bar">
            <router-link to="Login">Log In</router-link>
          </div>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>
<!--Estilos para incoporar en estilos-->
