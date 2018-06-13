<template>
</template>

<script>
import axios from 'axios';

const api_key = require('../../notas/token')
export default {
  name: 'FilmsComponent',
  components: {
  //  FilmsComponent,
  },
 
 data () {
   return {
     films: [],
     loading: false
   }
 }, 
 methods: {
   getFilms: function () {
     console.log('Estoy en getFilms');
     this.loading = true;
     axios.get("https://api.themoviedb.org/3/movie/76341?api_key=" + api_key.key)
     .then((response)  =>  {
       this.loading = false;
       this.films = response.data //.data.value;
       console.log('cucu desde llamada api');
       console.log(response)
     }, (error)  =>  {
       this.loading = false;
       console.log('Error cargando datos de la API');
     })
    }
  },
  mounted: function () {
      this.getFilms()
    }
};
</script>

<styles>
</styles>
