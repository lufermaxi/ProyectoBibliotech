<template>
  <div>
    <!-- Imagen de fondo -->
    <div class="vw-100 fondo-login">
      <!-- Color azul que cubre al fondo -->
      <div class="vh-100 recubrimiento d-flex justify-content-center">
        <!-- Contenedor invisible principal -->
        <b-container class="d-flex justify-content-center h-100">
          <!-- Tarjeta blanca -->
          <div class="contenedor-login ">
            <!-- Contenedor superior de la tarjeta blanca -->
            <div class="login-header mb-4">
              <img
                src="../assets/images/logo-minimal.png"
                alt=""
                fluid
                class="logo"
              />
            </div>
            <!-- Contenedor central de la tarjeta blanca -->
            <div class="login-inputs">
              <!-- Nombre de usuario -->
              <div class="form-floating mb-3">
                <input
                  type="username"
                  class="form-control"
                  id="floatingInput"
                  v-model="usuario"
                  placeholder="name@example.com"
                />
                <label for="floatingInput" class="text-secondary"
                  >Nombre de usuario</label
                >
                <b-form-text class="subtitulo" id="tags-remove-on-delete-help"
                  >Ingrese su nombre de usuario o e-mail</b-form-text
                >
              </div>
              <!-- Contraseña -->
              <div class="form-floating">
                <input
                  type="password"
                  class="form-control"
                  id="floatingPassword"
                  v-model="contraseña"
                  placeholder="Password"
                />
                <label for="floatingPassword" class="text-secondary"
                  >Contraseña</label
                >
                <b-form-text class="subtitulo" id="tags-remove-on-delete-help"
                  >Ingrese su contraseña</b-form-text
                >
              </div>
            </div>
            <!-- Contenedor inferior de la tarjeta blanca -->
            <div class="login-botones d-flex justify-content-end mt-4">
              <!-- boton de validacion -->
              <div class="boton-login">
                <b-button class="boton__entrar border-0" @click="ingresar()"
                  >Entrar</b-button
                >
              </div>
            </div>
          </div>
          <!-- atribucion de creative commons  -->
          <div class="cc-footer d-flex justify-content-end">
            <p>©2021 Bibliotech</p>
          </div>
        </b-container>
      </div>
    </div>
  </div>
</template>

<script>
import Swal from "sweetalert2";

export default {
  data() {
    return {
      url: "http://localhost:3000/api/login/",
      usuario: "",
      contraseña: "",
    };
  },
  methods: {
    async ingresar() {
      let parametros = { usuario: this.usuario, contraseña: this.contraseña };
      console.log(this.contraseña);
      await this.axios
        .post(this.url, JSON.parse(JSON.stringify(parametros)))
        .then((response) => {
          console.log(response.status);
          if (response.status == 200) {
            this.$router.push("Newer");
          }
        })
        .catch(() => {
          Swal.fire({
            icon: "error",
            title: "Oops...",
            text: "Usuario y/o contraseña incorrectos",
          });
        });
    },
  },
};
</script>

<style scoped>
.fondo-login {
  background-image: url("../assets/images/bg-img.jpg");
  box-sizing: border-box;
  background-repeat: no-repeat;
  z-index: 1;
}
.recubrimiento {
  background-color: #003482ea;
  z-index: 2;
}
.contenedor-login {
  background-color: #ffffff;
  z-index: 3;
  border-radius: 14px;
  width: 440px;
  height: 480px;
  padding: 10px;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
  margin-top: auto;
  margin-bottom: auto;
  position: relative;
  display: flex;
  justify-content: center;
  flex-direction: column;
}
.login-header {
  width: 100%;
  display: flex;
  justify-content: center;
  z-index: 2;
}
.logo {
  overflow: auto;
  box-sizing: border-box;
  padding: 10px;
}
.login-inputs {
  font-family: "Roboto", "Helvetica", "Arial", sans-serif;
  font-weight: 400;
  padding-left: 65px;
  padding-right: 65px;
}
.subtitulo {
  font-weight: 300;
  font-size: 0.75rem;
}
.login-botones {
  padding-left: 65px;
  padding-right: 65px;
}
.boton__entrar {
  background-color: #c30000;
  font-family: "Roboto", "Helvetica", "Arial", sans-serif;
  font-weight: 400;
  line-height: 18px;
}
.boton__entrar:hover {
  background-color: #990000;
}
.cc-footer {
  z-index: 2;
  display: flex;
  position: absolute;
  align-self: flex-end;
  padding-bottom: 10px;
}
.cc-footer p {
  font-family: "Roboto", "Helvetica", "Arial", sans-serif;
  font-size: 14px;
  font-weight: 300;
  color: #ffffff;
}
</style>
