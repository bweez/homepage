<template>
  <div class="bg">
    <div id="app">
      <div id="nav">
        <router-link to="/">0: Intro</router-link> |
        <router-link to="/about">1: Personal</router-link>  |
        <router-link to="/work">2: Professional</router-link>  |
        <router-link to="/wip">3: WIP</router-link>
      </div>
      <router-view />
    </div>
  </div>
</template>

<style lang="scss">
body, html {
  height: 100%;
}
.bg {
  /* Full height */
  height: 100%;
  background-color: #490966;
  background-image: url('../public/img/seattle/ben-dutton-insv5BSTqv0-unsplash-xl.jpg');
  background-blend-mode: screen;
  background-size: 100%;
  /* Center and scale the image nicely */
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
/*Image optimization for mobile*/
@media (max-width: 576px) {
    .bg {
      background-image: url('../public/img/seattle/ben-dutton-insv5BSTqv0-unsplash-m.jpg');
    }
  }

#app {
  font-family: Consolas,monaco,"Ubuntu Mono",courier,monospace;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #F0FFF1;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #F0FFF1;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
