<template>
  <nav id = "desktopNav">
    <router-link to="/about" class = "abt"><p class ="hover-underline-animation" >Contact</p></router-link>
    <router-link to="/about" class = "abt"><p class ="hover-underline-animation" >Mailing List</p></router-link>
    <router-link to="/about" class = "abt"><p class ="hover-underline-animation" >Social Media</p></router-link>
    <router-link to="/about" class = "abt"><p class ="hover-underline-animation" >About</p></router-link>
    <router-link to="/" class = "abt" ><p class ="hover-underline-animation" >Home</p></router-link>
  </nav>

  <div class ="container">
  <nav  id = "mobileNav">
      <input type="checkbox" name="menu" id="menu" class="menu-toggler">
      <label for="menu" class="menu-toggler-label">Menu</label>


    <ul class ="stagger-menu">
      <li class = "backgroundLI" style="--i: 0"></li>
      <li style="--i: 1"> <router-link to="/about" class = "abt" ><p class ="hover-underline-animation" >Contact</p></router-link></li>
      <li style="--i: 2"> <router-link to="/about" class = "abt" ><p class ="hover-underline-animation" >Mailing List</p></router-link></li>
      <li style="--i: 3"> <router-link to="/about" class = "abt"><p class ="hover-underline-animation" >Social Media</p></router-link></li>
      <li style="--i: 4"> <router-link to="/about" class = "abt" ><p class ="hover-underline-animation" >About</p></router-link></li>
      <li style="--i: 5"> <router-link to="/" class = "abt"><p class ="hover-underline-animation" >Home</p></router-link></li>

    </ul>
  </nav>
  </div>
  <router-view/>

</template>
<script>

  export default {
    data: function() {
      return {
        hidden: true,
      }
      
    },

    methods: {
 
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

  .container {
    overflow-x: hidden;
    z-index: 5;
    height: -webkit-fill-available;
    width: -webkit-fill-available;
    position: absolute;

  }

  @keyframes backgroundz {
    from {
      background-position: 0% center;
    }
    
    to {
      background-position: -200% center;
    }
  }
  .backgroundLI{
    animation: backgroundz 30s linear infinite;
    background: linear-gradient(
      to right,
      var(--g1),
      var(--g2),
      var(--g4),
      var(--g5),
      var(--g1)
    );
    background-size: 600%;
    height: -webkit-fill-available;
    width: -webkit-fill-available;
    overflow-x: hidden;
    margin: 0px;
    position: absolute;

  }
  .menu-toggler {
    display: none;
  }

  .menu-toggler-label {
    cursor: pointer;
    font-size: 20px;
    font-weight: bold;
    margin:0px;
    padding:0px;
    position: absolute;
    z-index: 5;

  }

  .stagger-menu {
    list-style-type: none;
    margin: 0px;
    padding: 0;
    height: -webkit-fill-available;
    width: -webkit-fill-available;
    overflow-x: hidden;
    overflow-y: hidden;
    text-align: center;

  }

  .stagger-menu li {
    margin-top: 0;
    font-size: 18px;
    opacity: 0;
    transform: translateX(100%);
    transition-property: opacity, transform;
    transition-duration: 0.3s;
    transition-timing-function: cubic-bezier(.6, -0.015, 0.565, 1.055);
  }

  .menu-toggler:checked ~ .stagger-menu li {
    opacity: 1;
    transform: translateX(0);
    transition-delay: calc(0.05s * var(--i));
  }
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
    text-align: center;
    width: 100%;

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
    z-index: -1;
    height: -webkit-fill-available;
    width: -webkit-fill-available;
    background-size: 600%;
    padding:0;
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
  .container{
    display: none;
  }
  }
  

</style>
