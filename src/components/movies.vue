<template lang="html">
<div class="container-fluid">
 <div class="row" >
   <div class="col-md-12">
		 <h3>Watch Harry Potter Complete Series </h3>
   
     <hr>
       <br>
     <div class="row">
 <div class="card col-md-3"v-for="(item,index) in movieList.Search" ::key="index"  >
	  <img class="card-img-top" :src="item.Poster" >
  <div class="container">
   <h5 class="card-title">{{item.Title}}</h5> 
		<p class="card-text">{{item.Year}}</p>
     <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#myModal">
    View Summary
  </button>
    </div>
    </div>

    </div>
   </div>

     <!-- The Modal -->
  <div class="modal fade" id="myModal">
    <div class="modal-dialog modal-lg">
      <div class="modal-content">
      
        <!-- Modal Header -->
        <div class="modal-header">
              <h4 class="modal-title" style="text-aling:center;">Harry Potter</h4>
          <button type="button" class="close" data-dismiss="modal">&times;</button>
        </div>
        
        <!-- Modal body -->
       <div class="modal-body">
         <h5 style="text-align: left;">SYNOPSIS</h5>
         <br>
         <p>Harry Potter is a British-American film series based on the eponymous novels by author J. K. Rowling. The series is distributed by Warner Bros. and consists of eight fantasy films, beginning with Harry Potter and the Philosopher's Stone (2001) and culminating with Harry Potter and the Deathly Hallows – Part 2 (2011).[2][3] A spin-off prequel series that will consist of five films started with Fantastic Beasts and Where to Find Them (2016), marking the beginning of the Wizarding World shared media franchise.</p>
         <h5 style="text-align: left;">Cast</h5>
         <br>
        
         <div class="row">
        <div class="col-md-12"
        <div class="col-md-3">
          <div class="card c1" style="border:none">
  <img class="card-img-top" src="https://m.media-amazon.com/images/M/MV5BMTg4NTExODc3Nl5BMl5BanBnXkFtZTgwODUyMDEzMDE@._V1_UY209_CR8,0,140,209_AL_.jpg" alt="Card image cap" height="80px" width="60px">
  <div class="card-body">
    <p class="card-text">Daniel Radcliffe.</p>
  </div>
</div>
        </div>
       
         <div class="col-md-3">
            <div class="card">
            <img class="card-img-top" src="https://m.media-amazon.com/images/M/MV5BMTQ3ODE2NTMxMV5BMl5BanBnXkFtZTgwOTIzOTQzMjE@._V1_UY317_CR21,0,214,317_AL__QL50.jpg" alt="Card image cap">
            <div class="card-body">
            <p class="card-text">Emma Watson.</p>
              </div>
          </div>
      
        </div>
        <div class="col-md-3">
                    <div class="card c2">
  <img class="card-img-top" src="https://m.media-amazon.com/images/M/MV5BMjI3MDA3NjA1N15BMl5BanBnXkFtZTcwMDcyMDYzNw@@._V1_UX140_CR0,0,140,209_AL_.jpg" alt="Card image cap">
  <div class="card-body">
    <p class="card-text"> Rupert Grint.</p>
  </div>
</div>
        </div>
        <div class="col-md-3">
                              <div class="card c2">
  <img class="card-img-top" src="https://m.media-amazon.com/images/M/MV5BMTY3OTc4MTgyN15BMl5BanBnXkFtZTcwNTAxNjA3Mg@@._V1_UY209_CR7,0,140,209_AL_.jpg" alt="Card image cap">
  <div class="card-body">
    <p class="card-text"> Michael Gambon</p>
  </div>
</div>
      
        </div>
       
           
         </div>
        </div>
        
        <!-- Modal footer -->
        <div class="modal-footer">
          <button type="button" class="btn btn-danger" data-dismiss="modal">Close</button>
        </div>
        
      </div>
    </div>
  </div>
  </div>
  </div>
</template>



<script>
import axios from 'axios';

export default {
    data(){
      
        return{
            movieList:[],
        }
    },
          mounted()
      {
      this.GetMovies()
      } ,  
      methods:{
         GetMovies(){

             axios.get('http://www.omdbapi.com/?s=harry%20potter&apikey=e0620bd4').then(success => {
               this.movieList=success.data
          })
           
         },
      }
    
}
</script>
<style scoped>
.card-img-top {
    width: 76%;
    height: 60%;
}

.card {
  /* Add shadows to create the "card" effect */
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
/* margin: 2px 2px; */
margin-top: 10px;
padding-left: 40px; 
}
.modal-title {
    margin-bottom: 0;
    line-height: 1.5;
   
    padding-left: 267px;
}

/* On mouse-over, add a deeper shadow */
.card:hover {
  box-shadow: 0 10px 26px 0 rgba(0,0,0,0.2);
}

/* Add some padding inside the card container */
.container {
  padding: 2px 8px;
}

</style>