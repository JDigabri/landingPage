<template>
  <nav id = "desktopNav">
    <router-link to="/about" class = "abt"><p class ="hover-underline-animation" >Contact</p></router-link>
    <router-link to="/about" class = "abt"><p class ="hover-underline-animation" >Mailing List</p></router-link>
    <router-link to="/about" class = "abt"><p class ="hover-underline-animation" >Social Media</p></router-link>
    <router-link to="/about" class = "abt"><p class ="hover-underline-animation" >About</p></router-link>
    <router-link to="/" class = "abt" ><p class ="hover-underline-animation" >Home</p></router-link>
  </nav>
  <nav id = "mobileNav">
    <router-link to="/about" class = "abt" id="mtext" v-on:click="hidden = !hidden; debug();"><p class ="hover-underline-animation" >Contact</p></router-link>
    <router-link to="/about" class = "abt" id="mtext1"  v-on:click="hidden = !hidden; debug();"><p class ="hover-underline-animation" >Mailing List</p></router-link>
    <router-link to="/about" class = "abt" id="mtext2"  v-on:click="hidden = !hidden; debug();"><p class ="hover-underline-animation" >Social Media</p></router-link>
    <router-link to="/about" class = "abt" id="mtext3"  v-on:click="hidden = !hidden;debug();"><p class ="hover-underline-animation" >About</p></router-link>
    <router-link to="/" class = "abt" id="mtext4"  v-on:click="hidden = !hidden; debug();"><p class ="hover-underline-animation" >Home</p></router-link>
  </nav>
  <router-view/>
  <div id = "three">
    <button v-on:click="hidden = !hidden; debug();">|||</button>  
  </div>
</template>
<script>

  export default {
    data: function() {
      return {
        hidden: true,
      }
      
    },

    methods: {
    debug() {
      if(this.hidden == false){
        document.getElementById("mobileNav").style.zIndex = "5";
        document.getElementById("mtext").style.display = "block";
        document.getElementById("mtext1").style.display = "block";
        document.getElementById("mtext2").style.display = "block";
        document.getElementById("mtext3").style.display = "block";
        document.getElementById("mtext4").style.display = "block";
      }
      else{
        document.getElementById("mobileNav").style.zIndex = "-1";
        document.getElementById("mtext").style.display = "none";
        document.getElementById("mtext1").style.display = "none";
        document.getElementById("mtext2").style.display = "none";
        document.getElementById("mtext3").style.display = "none";
        document.getElementById("mtext4").style.display = "none";
      }
      }
    } 
  }

</script>


<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
  }
  body{
    margin: 0px;
    overflow-y: hidden;
  }

  /* MOBILE VIEW */
  @media only screen and (max-width: 1200px) {
    nav {
    padding: 1.5rem;
    background-color: rgba(0, 0, 0, 0);
    position: fixed;
    bottom: 0px;
    position: absolute;
    display: inline-block;
  
  }
  
  nav a {
    font-weight: bold;
    color: #000000;
  }
  
  nav a.router-link-exact-active {
    color: #000000;
  }
  
  .keyzy{
    font-size: 5vw;
    text-decoration: none;
    padding-left: 5vh;
    padding-right: 5vh;
    text-align: center;
  
  }
  
  .abt{
  
    font-size: 5vw;
    text-decoration: none;
    padding-left: 5vh;
    padding-right: 5vh;
    text-align: center;
    display: none;
  
  }
  a:hover {
    color: rgb(0, 0, 0);
  }
  .hover-underline-animation {
    display: inline-block;
    position: relative;
    color: #000000;
  }
  
  .hover-underline-animation:after {
    content: '';
    position: absolute;
    width: 100%;
    transform: scaleX(0);
    height: 2px;
    bottom: 0;
    left: 0;
    background-color: #000000;
    transform-origin: bottom right;
    transition: transform 0.25s ease-out;
  }
  
  .hover-underline-animation:hover:after {
    transform: scaleX(1);
    transform-origin: bottom left;
  }
  #three{
    float: right;
    position: absolute;
    z-index: 6;

  }
  #desktopNav{
    display: none;
  }
  :root {
    --g1: rgb(216, 146, 15);
    --g2: rgb(21, 233, 222);
    --g4: rgb(149, 255, 149);
    --g5: rgb(255, 158, 218);
  }
  
  #mobileNav{
    background-color: white;
    background-size: 100%;
    z-index: -1;
    height: -webkit-fill-available;
    width: -webkit-fill-available;
    animation: background-pan 30s linear infinite;
    background: linear-gradient(
      to right,
      var(--g1),
      var(--g2),
      var(--g4),
      var(--g5),
      var(--g1)
    );
    background-size: 200%;
    overflow-x: hidden;
    overflow-y: hidden;
    position: absolute;

  }
  }


  /* COMPUTER VIEW */
  @media only screen and (min-width: 1200px) {
    nav {
    padding: 1.5rem;
    background-color: rgba(0, 0, 0, 0);
    position: fixed;
    bottom: 0px;
    position: absolute;
    left: 50%;
    top: 95%;
    transform: translate(-50%, -80%);
  
  }
  
  nav a {
    font-weight: bold;
    color: #000000;
  }
  
  nav a.router-link-exact-active {
    color: #000000;
  }
  
  .keyzy{
    font-size: 1vw;
    text-decoration: none;
    float:right;  
    padding-left: 1vh;
    padding-right: 1vh;
    text-align: center;
  
  }
  
  .abt{
  
    font-size: 1vw;
    text-decoration: none;
    float:right;  
    padding-left: 1vh;
    padding-right: 1vh;
    text-align: center;
  
  }
  a:hover {
    color: rgb(0, 0, 0);
  }
  .hover-underline-animation {
    display: inline-block;
    position: relative;
    color: #000000;
  }
  
  .hover-underline-animation:after {
    content: '';
    position: absolute;
    width: 100%;
    transform: scaleX(0);
    height: 2px;
    bottom: 0;
    left: 0;
    background-color: #000000;
    transform-origin: bottom right;
    transition: transform 0.25s ease-out;
  }
  
  .hover-underline-animation:hover:after {
    transform: scaleX(1);
    transform-origin: bottom left;
  }

  #three{
    display: none;
  }
  }
  

</style>
