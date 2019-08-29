<template>
  <div id="app">
   <!-- <nav class="navbar navbar-expand-lg " style="background-color:black;">
        <a class="navbar-brand" href="#">Movies Web</a>
          
      </nav> -->
      <!-- <Slide></Slide> -->
      <slide></slide>
      <movies  ></movies>
      <addmovies></addmovies>
      <br>
      <app-footer></app-footer>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import movies from './components/movies';
import addmovies from './components/addmovies';
 import slide from './components/slide';
 import footer from './components/footer';

export default {
  name: 'App',
  components: {
    HelloWorld,
    'slide':slide,
    'movies':movies,
    'addmovies':addmovies,
    'app-footer':footer,
     

  }
 

    

   
    
  
  
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}
</style>
