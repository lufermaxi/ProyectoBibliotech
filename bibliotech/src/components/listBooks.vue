<template>
    <div>
      <div class="title-format">
        <h3>Categoría: Ilustración</h3><!--Esta categoría se pinta con la lista y cambiar el nombre de categoría en la que se está-->
      </div> 
      <b-row class="row-books">
        <b-col cols="12" md="6" lg="2">
          <!--Libro 1-->
          <CardBook />
        </b-col>
        <b-col cols="12" md="6" lg="2">
          <!--Libro 2-->
          <CardBook />
        </b-col>
        <b-col cols="12" md="6" lg="2">
          <!--Libro 3-->
          <CardBook />
        </b-col>
        <b-col cols="12" md="6" lg="2">
          <!--Libro 4-->
          <CardBook />
        </b-col>
        <b-col cols="12" md="6" lg="2">
          <!--Libro 5-->
          <CardBook />
        </b-col>
        <b-col cols="12" md="6" lg="2">
          <!--Libro 6-->
          <CardBook />
        </b-col>
      </b-row>
    </div>
</template>
<script>
    import CardBook from "./cardBook.vue";
export default {
  components: {
    CardBook,
  },
};
</script>