<template>
  <div id="app">
    
    <div id="nav">
      
      <router-link to="/">Video TV</router-link > |

      <div id="addmv">
      <router-link to="/vermapa">Ver mapa</router-link> |
      <router-link to="/avideo">Agregar video</router-link>
      </div>
    </div>
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  
}

#nav {
  padding: 30px;
  margin: 15px;
  background-color: #fd5151;
  display: flex;
}

#addmv {
    padding-top: 15px;
    position: absolute;   
    left: 825px;
    font-size: 16px;
    top: 30px;
}

#nav a {
  font-weight: bold;
  color: white;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
