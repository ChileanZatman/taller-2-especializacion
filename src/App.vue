<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">brandname</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
        <div class="navbar-nav">
          <router-link to="/" class="nav-link" aria-current="page">Popular</router-link>
          <!-- <a class="nav-link active" aria-current="page" href="#">Home</a> -->
          <router-link to="/toprated" class="nav-link">Top rated</router-link>
        </div>
      </div>
    </div>
  </nav>
  <!-- <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/toprated">About</router-link>
  </div> -->
  <div class="container" style="background-color:#f0e4de;height:auto">
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
  background-color: #8c9778;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
