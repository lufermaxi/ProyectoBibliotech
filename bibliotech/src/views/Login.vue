<template>
  <div>
    <!-- Capa de color azul que cubre a la imagen de fondo -->
    <div class="recubrimiento"></div>

    <!-- Contenedor central blanco -->
    <main class="contenedor-login">
      <!-- Contenedor de los elementos de Login -->
      <div class="caja-login">
        <!-- Contenedor del logo -->
        <div class="contenedor-logo">
          <img src="../assets/images/logo-minimal.png" alt="" />
        </div>

        <!-- Cajas de Texto -->
        <div class="prueba-material">
          <form action="#">
            <!-- Nombre de usuario -->
            <div
              class="
                mdl-textfield mdl-js-textfield
                mdl-textfield--floating-label
              "
            >
              <input class="mdl-textfield__input" type="text" id="sample3" />
              <label class="mdl-textfield__label" for="sample3"
                >Nombre de usuario</label
              >
            </div>

            <br />

            <!-- Contraseña -->
            <div
              class="
                mdl-textfield mdl-js-textfield
                mdl-textfield--floating-label
              "
            >
              <input
                class="mdl-textfield__input"
                type="password"
                id="sample3"
              />
              <label class="mdl-textfield__label" for="sample3"
                >Contraseña</label
              >
            </div>

            <br />

            <div class="elementos-complementarios">
              <div class="forgot">
                <router-link to="Login">¿Olvidó su contraseña?</router-link>
              </div>

              <!-- Botón material (getmdl.io) -->
              <div class="contenedor-boton">
                <div class="boton-login">
                  <!-- Accent-colored raised button with ripple -->
                  <button
                    class="
                      mdl-button mdl-js-button
                      mdl-button--raised
                      mdl-js-ripple-effect
                      mdl-button--accent
                    "
                    type="button"
                  >
                    <router-link to="Newer">Entrar</router-link>
                  </button>
                </div>
              </div>
            </div>
          </form>
        </div>
      </div>

      <div class="cc-footer">
        <p>©2021 Bibliotech</p>
      </div>
    </main>
  </div>
</template>
