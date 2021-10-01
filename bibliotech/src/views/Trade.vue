<template>
  <div>
    <NavBar />
    <main class="main-section">
        <!--Inicio de la página de préstamo-->
        <section class="trade-section">
            <!--Inicio sección de saludo-->
            <div class="lineTrade-container">
                <h1>Solicitud</h1>
                <h3>de libro en préstamo</h3>
            </div>
        </section>
        <section class="wrapper-main">
            <section class="box-section">
                <!--Inicio sección caja de búsqueda de libros-->
                <div class="box-search">
                    <form action="ready"> <!--Aún no se especifica-->
                        <h4 class="search-text">Búsqueda de artículos: 
                            <input class="box" type="search" name="booksFormats" list="booksList">
                            <input class="button" type="submit" value="Buscar">
                        </h4>
                    </form>
                    <datalist id="booksList">
                        <option value="Digitales"></option>
                        <option value="Ilustración"></option>
                        <option value="Manuales"></option>
                        <option value="Revistas"></option>
                        <option value="Académicos"></option>
                    </datalist>
                </div>
            </section>
            <!--Inicio de galería de libros-->
            <section class="books-section">
                <!--Fila una de libros-->
                <div class="row-books">
                    <ul class="row-1">
                        <li class="book-one">
                            <!--Este link abrirá la ventana modal con la solicitud del libro-->
                            <a href="#view-one">
                                <img src="../assets/images/illustrated/book-one.png" alt="Los cuentos como son">
                            </a>
                            <!--Ventana modal petición de solicitud-->
                            <div id="view-one" class="modal">
                                <div class="modal-view">
                                    <a href="#">Regresar</a>
                                    <div class="info-book">
                                        <figure>
                                            <img src="../assets/images/illustrated/book-one.png" alt="Los cuentos como son">
                                        </figure>
                                        <p>Formato: Ilustración <br>Los cuentos como son
                                            <br>Rudyard Kipling <br>2021 <br>Alfaguara IJ
                                            <br>ISBN 978-84-204-5665-2
                                            <br><b>Disponible</b>
                                        </p>
                                    </div>
                                    <div class="book-btn">
                                    <a href="#view-confirmed1">Solicitar</a>
                                    </div>
                                </div>
                            </div>
                            <!--Crear un espacio de loading... para confirmar al cliente con vue-->
                            
                            <!--Ventana modal confirmación de préstamo-->
                            <div id="view-confirmed1" class="modal">
                                <div class="confirmed-view">
                                    <div class="info-book">
                                        <figure>
                                            <img src="../assets/images/illustrated/book-one.png" alt="Los cuentos como son">
                                        </figure>
                                    </div>
                                    <div class="confirmed-box">
                                        <p class="confirmed-text">¡Su préstamo ha sido exitoso!</p>
                                        <div class ="confirmed-icon">
                                            <h3>&#10004;</h3> <!--Reemplazar con ícono-->
                                        </div> 
                                        <div class="confirmed-btn">
                                            <a href="#">Ok</a>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </li>

                        <li class="book-two">
                            <a href="#view-two">
                                <img src="../assets/images/illustrated/book-two.png" alt="Harry Potter">
                            </a>
                            <!--Ventana modal-->
                            <div id="view-two" class="modal">
                                <div class="modal-view-two">
                                    <a href="#">Regresar</a>
                                    <div class="info-book-two">
                                        <figure>
                                            <img src="../assets/images/illustrated/book-two.png" alt="Harry Potter">
                                        </figure>
                                        <p>Formato: Ilustración <br>Harry Potter: And the goblet of fire
                                            <br>J.K. Rowling <br>2016 <br>Pottermore
                                            <br>ISBN 978-1-78110-567-2
                                            <br><b>Disponible</b>
                                        </p>
                                    </div>
                                    <div class="book-btn">
                                        <!--Queda por crear la ventana modal del formulario de datos del cliente-->
                                        <a href="#view-confirmed2">Solicitar</a>
                                    </div>
                                </div>
                            </div>
                            <!--Ventana modal confirmación de préstamo-->
                            <div id="view-confirmed2" class="modal">
                                <div class="confirmed-view2">
                                    <div class="info-book">
                                        <figure>
                                            <img src="../assets/images/illustrated/book-two.png" alt="Harry Potter">
                                        </figure>
                                    </div>
                                    <div class="confirmed-box">
                                        <p class="confirmed-text">¡Su préstamo ha sido exitoso!</p>
                                        <div class ="confirmed-icon">
                                            <h3>&#10004;</h3> <!--Reemplazar con ícono-->
                                        </div> 
                                        <div class="confirmed-btn">
                                            <a href="#">Ok</a>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </li>

                        <li class="book-three">
                            <a href="#view-three">
                                <img src="../assets/images/illustrated/book-three.png" alt="The squirrels">
                            </a>
        
                            <!--Ventana modal-->
                            <div id="view-three" class="modal">
                                <div class="modal-view-three">
                                    <a href="#">Regresar</a>
                                    <div class="info-book-three">
                                        <figure>
                                            <img src="../assets/images/illustrated/book-three.png" alt="The squirrels">
                                        </figure>
                                        <p>Formato: Ilustración <br>The squirrels who squabbled
                                            <br>Rachel Bright, Jim Field <br>2017 <br>Orchard Books
                                            <br>ISBN 978-1-40834-048-6
                                            <br><b>Disponible</b>
                                        </p>
                                    </div>
                                    <div class="book-btn">
                                        <a href="#view-confirmed3">Solicitar</a>
                                    </div>
                                </div>
                            </div>
                            <!--Ventana modal confirmación de préstamo-->
                            <div id="view-confirmed3" class="modal">
                                <div class="confirmed-view3">
                                    <div class="info-book">
                                        <figure>
                                            <img src="../assets/images/illustrated/book-three.png" alt="The squirrels">
                                        </figure>
                                    </div>
                                    <div class="confirmed-box">
                                        <p class="confirmed-text">¡Su préstamo ha sido exitoso!</p>
                                        <div class ="confirmed-icon">
                                            <h3>&#10004;</h3> <!--Reemplazar con ícono-->
                                        </div> 
                                        <div class="confirmed-btn">
                                            <a href="#">Ok</a>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </li>


                        <li class="book-four">
                            <a href="#view-four">
                                <img src="../assets/images/illustrated/book-four.png" alt="Viaje al centro">
                            </a>
                            <!--Ventana modal-->
                            <div id="view-four" class="modal">
                                <div class="modal-view-four">
                                    <a href="#">Regresar</a>
                                    <div class="info-book-four">
                                        <figure>
                                            <img src="../assets/images/illustrated/book-four.png" alt="Viaje al centro">
                                        </figure>
                                        <p>Formato: Ilustración <br>Viaje al centro de la tierra
                                            <br>Julio Verne <br>2004 <br>Panamericana Editorial
                                            <br>ISBN 978-9-58300-688-3
                                            <br><b>Disponible</b>
                                        </p>
                                    </div>
                                    <div class="book-btn">
                                        <!--Queda por crear la ventana modal del formulario de datos del cliente-->
                                        <a href="#view-confirmed4">Solicitar</a>
                                    </div>
                                </div>
                            </div>
                            <!--Ventana modal confirmación de préstamo-->
                            <div id="view-confirmed4" class="modal">
                                <div class="confirmed-view4">
                                    <div class="info-book">
                                        <figure>
                                            <img src="../assets/images/illustrated/book-four.png" alt="Viaje al centro">
                                        </figure>
                                    </div>
                                    <div class="confirmed-box">
                                        <p class="confirmed-text">¡Su préstamo ha sido exitoso!</p>
                                        <div class ="confirmed-icon">
                                            <h3>&#10004;</h3> <!--Reemplazar con ícono-->
                                        </div> 
                                        <div class="confirmed-btn">
                                            <a href="#">Ok</a>
                                        </div>
                                    </div>
                                </div>
                            </div>
                                
                        </li>

                        <li class="book-five">
                            <a href="#view-five">
                                <img src="../assets/images/illustrated/book-five.png" alt="Writing the future">
                            </a>
                            <!--Ventana modal-->
                            <div id="view-five" class="modal">
                                <div class="modal-view-five">
                                    <a href="#">Regresar</a>
                                    <div class="info-book-five">
                                        <figure>
                                            <img src="../assets/images/illustrated/book-five.png" alt="Writing the future">
                                        </figure>
                                            <p>Formato: Ilustración <br>Writing the Future: <br>Basquiat and the Hip-Hop Generation
                                            <br>J. Faith Almiron <br>2020 <br>MFA Publications
                                            <br>ISBN 978-0-87846-871-3
                                            <br><b>Disponible</b>
                                        </p>
                                    </div>
                                    <div class="book-btn">
                                        <!--Queda por crear la ventana modal del formulario de datos del cliente-->
                                        <a href="#view-confirmed5">Solicitar</a>
                                    </div>
                                </div>
                            </div> 
                            <!--Ventana modal confirmación de préstamo-->
                            <div id="view-confirmed5" class="modal">
                                <div class="confirmed-view5">
                                    <div class="info-book">
                                        <figure>
                                            <img src="../assets/images/illustrated/book-five.png" alt="Writing the future">
                                        </figure>
                                    </div>
                                    <div class="confirmed-box">
                                        <p class="confirmed-text">¡Su préstamo ha sido exitoso!</p>
                                        <div class ="confirmed-icon">
                                            <h3>&#10004;</h3> <!--Reemplazar con ícono-->
                                        </div> 
                                        <div class="confirmed-btn">
                                            <a href="#">Ok</a>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </li>

                        <li class="book-six">
                            <a href="#view-six">
                                <img src="../assets/images/illustrated/book-six.png" alt="Batman">
                            </a>
                            <!--Ventana modal-->
                            <div id="view-six" class="modal">
                                <div class="modal-view-six">
                                    <a href="#">Regresar</a>
                                    <div class="info-book-six">
                                        <figure>
                                            <img src="../assets/images/illustrated/book-six.png" alt="Batman">
                                        </figure>
                                            <p>Formato: Ilustración <br>Bataman: Streets of Gotham 
                                            <br>Paul Dini <br>2011 <br>DC Comics
                                            <br>ISBN 978-1-40122-722-7 
                                            <br><b>Disponible</b>
                                        </p>
                                    </div>
                                    <div class="book-btn">
                                        <!--Queda por crear la ventana modal del formulario de datos del cliente-->
                                        <a href="#view-confirmed6">Solicitar</a>
                                    </div>
                                </div>
                            </div> 
                            <!--Ventana modal confirmación de préstamo-->
                            <div id="view-confirmed6" class="modal">
                                <div class="confirmed-view6">
                                    <div class="info-book">
                                        <figure>
                                            <img src="../assets/images/illustrated/book-six.png" alt="Batman">
                                        </figure>
                                    </div>
                                    <div class="confirmed-box">
                                        <p class="confirmed-text">¡Su préstamo ha sido exitoso!</p>
                                        <div class ="confirmed-icon">
                                            <h3>&#10004;</h3> <!--Reemplazar con ícono-->
                                        </div> 
                                        <div class="confirmed-btn">
                                            <a href="#">Ok</a>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </li>
                    </ul>
                </div>
            </section>
        </section>
        <!-- fin libros o articulos que se van a listar-->
    </main>
    <Footer />
  </div>
</template>
<script>
import NavBar from '../components/navbar.vue'
import Footer from '../components/footer.vue'

export default {
  components: {
    NavBar,
    Footer,
  },
};
</script>
