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
                <span class="material-icons material-icons--boton-sup"
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
      <!-- FIN Parte superior (Migas de pan y botones) -->

      <!-- Contenido luego de las migas de pan (Cartas) -->
      <div class="seccion-central">
        <!-- Grilla dinamica -->
        <div class="grilla-responsive">
          <!-- Carta para listar elementos -->
          <div class="carta">
            <!-- Seccion superior de la carta -->
            <div class="carta-header">
              <div class="carta-header__texto">
                <p class="carta-header__texto carta-header__texto--titulo">
                  Nombre del Articulo
                </p>
                <p class="carta-header__texto carta-header__texto--subtitulo">
                  Nombre del Autor
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
                <a
                  class="carta-footer__botones carta-footer__botones--cancelar"
                  href="item.html"
                  >BORRAR</a
                >
                <input
                  class="carta-footer__botones carta-footer__botones--boton"
                  type="submit"
                  value="EDITAR"
                />
              </div>
            </div>
          </div>
          <!-- FIN Carta para listar elementos -->

          <!-- Carta para listar elementos -->
          <div class="carta">
            <!-- Seccion superior de la carta -->
            <div class="carta-header">
              <div class="carta-header__texto">
                <p class="carta-header__texto carta-header__texto--titulo">
                  Nombre del Articulo
                </p>
                <p class="carta-header__texto carta-header__texto--subtitulo">
                  Nombre del Autor
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
                <a
                  class="carta-footer__botones carta-footer__botones--cancelar"
                  href="item.html"
                  >BORRAR</a
                >
                <input
                  class="carta-footer__botones carta-footer__botones--boton"
                  type="submit"
                  value="EDITAR"
                />
              </div>
            </div>
          </div>
          <!-- FIN Carta para listar elementos -->

          <!-- Carta para listar elementos -->
          <div class="carta">
            <!-- Seccion superior de la carta -->
            <div class="carta-header">
              <div class="carta-header__texto">
                <p class="carta-header__texto carta-header__texto--titulo">
                  Nombre del Articulo
                </p>
                <p class="carta-header__texto carta-header__texto--subtitulo">
                  Nombre del Autor
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
                <a
                  class="carta-footer__botones carta-footer__botones--cancelar"
                  href="item.html"
                  >BORRAR</a
                >
                <input
                  class="carta-footer__botones carta-footer__botones--boton"
                  type="submit"
                  value="EDITAR"
                />
              </div>
            </div>
          </div>
          <!-- FIN Carta para listar elementos -->

          <!-- Carta para listar elementos -->
          <div class="carta">
            <!-- Seccion superior de la carta -->
            <div class="carta-header">
              <div class="carta-header__texto">
                <p class="carta-header__texto carta-header__texto--titulo">
                  Nombre del Articulo
                </p>
                <p class="carta-header__texto carta-header__texto--subtitulo">
                  Nombre del Autor
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
                <a
                  class="carta-footer__botones carta-footer__botones--cancelar"
                  href="item.html"
                  >BORRAR</a
                >
                <input
                  class="carta-footer__botones carta-footer__botones--boton"
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
      <!-- FIN Contenido luego de las migas de pan (Cartas) -->
    </main>
    <!-- FIN Contenido principal de la pagina -->
  </div>
</template>
<script>
import SideBar from '../components/sidebar.vue'

export default {
  components: {
    SideBar
  }
}
</script>
