<template>
  <nav>
    <router-link to="/" class = "keyzy" ><p class ="hover-underline-animation" >Home</p></router-link>
    <router-link to="/about" class = "abt"><p class ="hover-underline-animation" >About</p></router-link>
    <router-link to="/about" class = "abt"><p class ="hover-underline-animation" >About</p></router-link>
    <router-link to="/about" class = "abt"><p class ="hover-underline-animation" >About</p></router-link>
    <router-link to="/about" class = "abt"><p class ="hover-underline-animation" >About</p></router-link>

  </nav>
  <router-view/>
  
</template>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
body{
  margin: 0px;

}
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
</style>
