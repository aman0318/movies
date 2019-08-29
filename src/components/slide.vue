<template>

<div class="mainscreen">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.8.2/css/all.css">

    <video autoplay loop muted id="bg" width="100%">
     <source src="https://mdbootstrap.com/img/video/Tropical.mp4" type="video/mp4" />
    </video>
    <p id="icon" v-animate-css="'bounceInLeft'"><i class="fas fa-video"> Play  Movies</i></p>

    <div class="text-img" >
    <h2 class="info-img-text1">Looking For a Movie.....</h2> 
	<br>   
  
    <h2 class="info-img-text2">Just Scroll Down  <i class="fas fa-sort-down" style="font-size:70px;"></i> </h2> 
    </div>
    
      
</div>

</template>

<style scoped>

    *{
        padding: 0px;
        margin: 0px;
        
    }

    #bg
    {
       position: relative;
       top: 0px;
       left: 0px;
       z-index: -999;
     
    }
    #icon
    {
      color: rgb(255, 255, 255);
      position: absolute;
      top: 10px;
      font-size: 400%;
      padding-left: 150px;
      padding-top: 30px;
      padding-right: 10px; 
    }

    p::after{
      
      font-size: 55px;
      padding-left: 30px;
      position: absolute;
      top: 40px;
      color: rgb(255, 255, 255);
    }

    .info-img-text1
    {
      position: absolute;
          top: 123px;
    left: 690px;
      color: white;
    }
   .info-img-text2
    {
      position: absolute;
          top: 153px;
    left: 890px;
      color: white;
    }

</style>