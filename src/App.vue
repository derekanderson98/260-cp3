<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
      <h1>Apocalypse Status</h1>
    </div>
    <router-view/>

    <div class="spacer"></div>
    <p class="footer-container"><a class="footer" href="https://github.com/derekanderson98/260-cp3">
    github repository for this project</a></p>

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
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: red;
}

.spacer {
    height: 5em;
}

.footer-container {
    background-color: gray;
    padding: 8px 16px;
    position: fixed;
    bottom: 0;
    width: 100%;
    margin: 0px;
    text-align: left;
}

.footer {
    color: black;
    text-decoration: none;
}

.footer:hover {
    color: darkgray;
}
</style>
