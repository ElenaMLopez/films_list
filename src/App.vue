<template>
  <div id="app">
    <FilmsHeader />
    <FilmsComponent />
  </div>
</template>

<script>
import axios from 'axios';
import FilmsHeader from './components/header.vue';
import FilmsComponent from './components/films_component.vue';



export default {
  name: 'app',
  components: {
    FilmsHeader,
    FilmsComponent,
  },
 
 data () {
   return {
     films: [],
     loading: false
   }
 }, 
 // methods: {
 //   getFilms: function () {
 //     console.log('Estoy en getFilms');
 //     this.loading = true;
 //     axios.get("https://api.themoviedb.org/3/movie/76341?api_key=2b072647db7f748846798db37c85bf9e")
 //     .then((response)  =>  {
 //       // this.loading = false;
 //       // this.films = response //.data.value;
 //       console.log('cucu desde llamada api')
 //     }, (error)  =>  {
 //       this.loading = false;
 //       console.log('Error cargando datos de la API');
 //     })
 //    }
 //  },
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
