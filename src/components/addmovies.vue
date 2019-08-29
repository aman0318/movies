<template lang="html">
<div class="container-fluid">
     <h1 id="title">{{add}}</h1>
 <p class="slant"></p>
 <div class="row">
     <!-- <div class="col-md-12 Back-Img"> -->
         <div class="col-md-6 card">
          <form   >
             
                <div class="form-group ">
                    <label style="padding-top:20px;" >{{Name}}</label><br>
                    <input type="text" id="int-name" placeholder="Enter Movie Title..." v-model="MovieTitle" >
                </div>
                <div class=" form-group">
                    <label >{{MovieSummarys}}</label><br>
                    <input type="text"  id="int-summ"  placeholder="Enter Movie Summary" v-model="MovieSummary">
                </div>
                <div class=" form-group">
                    <label >Movie Image</label><br>
                    <input type="text"  id="int-Img"  placeholder="Enter Image Url" v-model="PosterImg">
                 </div>
             

          </form>
           <div class="form-group" >
            <button id="btn-form" v-on:click="addMovie"   >Add Movie</button>
        </div> 
         </div>
         <div class="col-md-6">

           <h5 style="padding-top:20px;"> Peview Of Inputs</h5>
           <hr>
            
        <div class="demo">
          <div id="M-name">
              <p>Movie Title: {{MovieTitle}}</p>
            
          </div>
          <div id="M-Summ">
              <p>Movie Summary: {{MovieSummary}}</p>
            
          </div>
          <div id="M-Summ">
              <p>Image URL: {{PosterImg}}</p>
             
            
          </div>
          <br>
          
        </div>
          
          
        

         </div>

     </div>
      <h1 id="title">{{Newadd}}</h1>
 <p class="slant"></p>
     <div class="row">
     
  <div class="col-md-12">
     <div class="row">
 <div class="card col-md-3" v-for="(movie,index) in addedMovieList " ::key="index" v-if="index >0" >
	  <img class="card-img-top" :src="movie.Poster" >
      <br>
  <div class="container">
   <h5 class="card-title">{{movie.Title}}</h5> 
		<p class="card-text">{{movie.Summary}}</p>
    </div>
    </div>

    </div>
   </div>
     </div>

 

</div>
       
</template>

 <script>
 export default {
       data(){
      
        return{
           addedMovieList:[],
           add:"Add Your Movies",
           Name:" Movie Title",
           MovieSummarys:"Movie Summary",
           MovieTitle:'',
           MovieSummary:'',
           PosterImg:'',
           Newadd:"Latest Movies",

        }
    },
       mounted()
       {
    
       this.addMovie()
     } ,
    methods:{
        addMovie(){
          
           this.addedMovieList.push({
        
        Title:this.MovieTitle,
        Summary:this.MovieSummary,
        Poster:this.PosterImg,
        
      })
        }
    }
 }
 </script>
        <style scoped>
          #title
{
    height: 12vh;
    text-align: center;
    margin-top: 2%;
    padding-top: 20px;
    font-size: 34px;
    color:white;
    position: relative;
    background: rgb(27, 219, 253);
}

label
{

    margin-left:0px;
    text-align: left;
    color:black;
   
}
.card{
    border-left: 0px;
    border-top:0px;
    border-bottom: 0px;
}

input
{
    width: 200px;
    height: 40px;
    border-radius: 4px;
   
}
input:hover
{
    width: 300px;
    transition: width 1s;
}
#btn-form
{
   
    
    border: 1px solid white;
    padding: 10px 18px;
    margin-top: 20px;
    border-radius: 4px;
    color: white;
   background: rgb(27, 219, 253);
    font-size: 18px;
}

        
        </style>