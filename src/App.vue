<template>
  <nav>
    <router-link to="/" class = "keyzy">KeyZy</router-link>
    <router-link to="/about" class = "abt">About</router-link>
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
  padding: 3.23vh;
  background-color: black;
  position: sticky;
}

nav a {
  font-weight: bold;
  color: #FFFFFF;
}

nav a.router-link-exact-active {
  color: #FFFFFF;
}

.keyzy{
  text-align: left;
  font-size:3vh;
  text-decoration: none;
}

.abt{
  font-size: 3vh;
  text-decoration: none;
  float:right;  
}

</style>
