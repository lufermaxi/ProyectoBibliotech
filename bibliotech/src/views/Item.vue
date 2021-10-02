<template>
  <div class="cuerpo">
    <SideBar />
    <!-- Contenido principal de la pagina -->
    <main class="contenido">
      <!-- Parte superior (Migas de pan y botones) -->
      <div class="barra-superior">
        <div class="contenedor-superior">
          <!-- Migas de pan -->
          <div class="contenedor-migasdepan">
            <p class="miga2 migas__principal--texto">Artículos</p>
            <p class="separador migas__principal--texto">|</p>
          </div>
          <!-- FIN Migas de pan -->

          <!-- Botones con funciones -->
          <div class="contenedor-botonessuperiores">
            <!-- Boton para crear elementos -->
            <div class="boton__crear">
              <div class="icono-superior">
                <span
                  class="material-icons material-icons--boton-sup"
                  @click="formNuevo()"
                  >add</span
                >
              </div>
            </div>

            <!-- Botones implementados para futuras funciones

                    <div class="boton__editar" >
                        <div class="icono-superior">
                            <span class="material-icons material-icons--boton-sup-fixed">edit</span>
                        </div>
                    </div>
                    Boton para seleccionar elementos
                    <div class="boton__seleccionar">
                        <div class="icono-superior">
                            <span class="material-icons material-icons--boton-sup">library_add</span>
                        </div>
                    </div>

                    Boton para borrar elementos
                    <div class="boton__borrar"></div>
                        <div class="icono-superior">
                            <span class="material-icons material-icons--boton-sup">delete</span>
                        </div>
                    </div> -->
            <!-- FIN Botones con funciones -->
          </div>
        </div>
      </div>
      <div v-if="activar != false">
        <!-- Formulario para creación de Articulos -->
        <div class="seccion-central">
          <!-- Recuadro que contiene a todos los elementos del formulario -->
          <div class="formulario-base">
            <!-- Segmento izquiero del contenedor -->
            <div class="formulario-base-lado1">
              <label for="isbn">ISBN:</label>
              <input
                type="text"
                id="isbn"
                v-model="articulo.isbn"
                name="isbn"
              />

              <label for="nombre-articulo">Nombre del artículo:</label>
              <input
                type="text"
                id="nombre-articulo"
                v-model="articulo.nombre"
                name="nombre-articulo"
              />

              <label for="nombre-autor">Nombre del autor:</label>
              <input
                type="text"
                id="nombre-autor"
                v-model="articulo.nombre_autor"
                name="nombre-autor"
              />
            </div>
            <!-- FIN Segmento izquero del contenedor -->

            <!-- Segmento derecho del contenedor -->
            <div class="formulario-base-lado2">
              <label for="nombre-editorial">Nombre de la editorial:</label>
              <input
                type="text"
                v-model="articulo.nombre_editorial"
                id="nombre-editorial"
                name="nombre-editorial"
              />

              <label for="nombre-editorial">Seleccione una categoria:</label>
              <select
                name="categoria"
                v-model="articulo.nombre_categoria"
                id="categoria"
              >
                <option value=""></option>
                <option value="Académico">Académico</option>
                <option value="Digital">Digital</option>
                <option value="Ilustración">Ilustración</option>
                <option value="Manual">Manual</option>
                <option value="Revista">Revista</option>
              </select>
            </div>
            <!-- FIN Segmento derecho del contenedor -->

            <!-- Sección inferior del contenedor -->
            <div class="contenedor-formulario-footer">
              <div class="contenedor-botones">
                <a class="enlace-cancelar" @click="cancelar()">CANCELAR</a>
                <input
                  class="formulario__boton-crear"
                  type="submit"
                  @click="guardar()"
                  value="CREAR"
                />
              </div>
            </div>
            <!-- FIN Sección inferior del contenedor -->
          </div>
          <!-- FIN Recuadro que contiene a todos los elementos del formulario -->
        </div>
        <!-- FIN Formulario para creación de Articulos -->
      </div>
      <!-- FIN Parte superior (Migas de pan y botones) -->
      <span v-for="articulo in articulos" :key="articulo.id">
        <div class="seccion-central">
          <!-- Grilla dinamica -->
          <div class="grilla-responsive">
            <!-- Carta para listar elementos -->

            <div class="carta">
              <!-- Seccion superior de la carta -->
              <div class="carta-header">
                <div class="carta-header__texto">
                  <p class="carta-header__texto carta-header__texto--titulo">
                    {{ articulo.nombre }}
                  </p>
                  <p class="carta-header__texto carta-header__texto--titulo">
                    {{ articulo.nombre_autor }}
                  </p>
                </div>
              </div>

              <!-- Seccion central de la carta -->
              <div class="carta-body">
                <div class="carta-body__imagen">
                  <img src="../assets/images/illustrated/book-one.png" alt="" />
                </div>
              </div>

              <!-- Seccion inferior de la carta -->
              <div class="carta-footer">
                <div class="carta-footer__botones">
                  <button
                    class="carta-footer__botones carta-footer__botones--cancelar"
                    @click="borrar(articulo.id)"
                  >
                    BORRAR
                  </button>
                  <input
                    class="carta-footer__botones carta-footer__botones--boton"
                    @click="
                      formEditar(
                        articulo.id,
                        articulo.nombre,
                        '0',
                        articulo.nombre_editorial,
                        articulo.nombre_autor,
                        articulo.nombre_categoria,
                        articulo.isbn
                      )
                    "
                    type="submit"
                    value="EDITAR"
                  />
                </div>
              </div>
            </div>
            <!-- FIN Carta para listar elementos -->
          </div>
          <!-- FIN Grilla dinamica -->
        </div>
      </span>
      <!-- FIN Contenido luego de las migas de pan (Cartas) -->
    </main>
    <!-- FIN Contenido principal de la pagina -->
  </div>
</template>
<script>
import SideBar from "../components/sidebar.vue";

export default {
  components: {
    SideBar,
  },
  data() {
    return {
      url: "http://localhost:3000/api/articulos/",
      articulos: [],
      operacion: "",
      activar: false,
      articulo: {
        id: null,
        nombre: "",
        prestamo: "",
        nombre_editorial: "",
        nombre_autor: "",
        nombre_categoria: "",
        isbn: "",
      },
    };
  },
  created() {
    this.mostrar();
  },
  methods: {
    mostrar() {
      this.axios.get(this.url).then((response) => {
        this.articulos = response.data;
      });
    },
    borrar(id) {
      this.axios.delete(this.url + id).then((response) => {
        this.mostrar();
      });
    },
    crear () {
      let parametros = {
        nombre: this.articulo.nombre,
        prestamo: '0',
        nombre_editorial: this.articulo.nombre_editorial,
        nombre_autor: this.articulo.nombre_autor,
        nombre_categoria: this.articulo.nombre_categoria,
        isbn: this.articulo.isbn,
      };
      this.axios.post(this.url, parametros).then((response) => {
        this.mostrar();
      });
      this.articulo.nombre = "";
      this.articulo.prestamo= "";
      this.articulo.nombre_editorial = "";
      this.articulo.nombre_autor = "";
      this.articulo.nombre_categoria = "";
      this.articulo.isbn = "";
    },
    editar () {
      let parametros = {
        nombre: this.articulo.nombre,
        prestamo: this.articulo.prestamo,
        nombre_editorial: this.articulo.nombre_editorial,
        nombre_autor: this.articulo.nombre_autor,
        nombre_categoria: this.articulo.nombre_categoria,
        isbn: this.articulo.isbn,
        id: this.articulo.id,
      };
      this.axios.put(this.url + this.articulo.id, parametros).then((response) => {
        this.mostrar();
      });
    },
    //formularios y botones
    guardar() {
      if (this.operacion == "crear") {
        this.crear();
      }
      if (this.operacion == "editar") {
        this.editar();
      }
      this.activar = false;
    },
    cancelar() {
      this.activar = false;
    },
    formNuevo() {
      this.activar = true;
      this.operacion = "crear";
      this.articulo.nombre = "";
      this.articulo.prestamo = "0";
      this.articulo.nombre_editorial = "";
      this.articulo.nombre_autor = "";
      this.articulo.nombre_categoria = "";
      this.articulo.isbn = "";
    },
    formEditar(
      id,
      nombre,
      prestamo,
      nombre_editorial,
      nombre_autor,
      nombre_categoria,
      isbn
    ) {
      this.articulo.id = id;
      this.articulo.nombre = nombre;
      this.articulo.prestamo = prestamo;
      this.articulo.nombre_editorial = nombre_editorial;
      this.articulo.nombre_autor = nombre_autor;
      this.articulo.nombre_categoria = nombre_categoria;
      this.articulo.isbn = isbn;
      this.activar = true;
      this.operacion = "editar";
    },
  },
};
</script>
