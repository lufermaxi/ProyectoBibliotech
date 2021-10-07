<template>
  <div>
    <!-- Barra de navegación lateral -->
    <aside class="barra-lateral">
      <!-- Grupo de elementos #1 -->
      <div class="contenedor-header">
        <!-- Contenedor logo -->
        <div class="contenedor-header__logo">
          <img src="../assets/images/logo-minimal.png" alt="Logo Bibliotech" />
        </div>

        <!-- Contenedor de usuario actual -->
        <div class="contenedor-header__usuario">
          <div class="header__usuario">
            <!-- Nombre de usuario actual -->
            <p class="usuario_titulo">Nombre de usuario</p>

            <!-- Tipo de usuario actual -->
            <div class="header__usuario-label">
              <div class="header__usuario-label-texto">root</div>
            </div>
          </div>
        </div>
      </div>
      <!-- FIN Grupo de elementos #1 -->

      <!-- Grupo de elementos #2 -->
      <div class="contenedor-body-1">
        <!-- Primer elemento de la barra lateral -->
        <div class="contenedor-barra-1 contenedor-barra-1--actual">
          <div class="elemento-1">
            <div class="elemento-1__icono">
              <span
                class="material-icons material-icons--settings-actual"
              ></span>
            </div>
            <p class="elemento-1__titulo elemento-1__titulo--actual">
              <router-link to="Newer">Recientes</router-link>
            </p>
          </div>
        </div>

        <!-- Segundo elemento de la barra lateral -->
        <div class="contenedor-barra-2 ">
          <div class="elemento-1">
            <div class="elemento-1__icono">
              <span class="material-icons material-icons--settings"></span>
            </div>
            <p class="elemento-1__titulo ">
              <router-link to="Item">Articulos</router-link>
            </p>
          </div>
        </div>

        <!-- Tercer elemento de la barra lateral -->
        <div class="contenedor-barra-3">
          <div class="elemento-1">
            <div class="elemento-1__icono">
              <span class="material-icons material-icons--settings"></span>
            </div>
            <p class="elemento-1__titulo">
              <router-link to="Admin">Administradores</router-link>
            </p>
          </div>
        </div>
      </div>
      <!-- FIN Grupo de elementos #2 -->

      <!-- Grupo de elementos #3 -->
      <div class="contenedor-body-2">
        <!-- Tercer elemento de la barra lateral -->
        <div class="contenedor-barra-1">
          <div class="elemento-1">
            <div class="elemento-1__icono">
              <span class="material-icons material-icons--settings"></span>
            </div>
            <p class="elemento-1__titulo">
              <router-link to="Login">Salir</router-link>
            </p>
          </div>
        </div>
      </div>
      <!-- FIN Grupo de elementos #3 -->
    </aside>
    <!-- FIN Barra de navegación lateral -->
  </div>
</template>
