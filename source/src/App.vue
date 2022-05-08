<template>
  <div class="d-flex flex-column flex-md-row align-items-center p-3 px-md-4 mb-3 bg-white">
    <h5 class="my-0 mr-md-auto font-weight-normal">Vue mini project</h5>
    <nav class="my-2 my-md-0 mr-md-3">
      <router-link to="/products">Product manager</router-link>
      <router-link to="/users">User manager</router-link>
    </nav>
    <a href="" routerlink="cart">Admin</a>
  </div>

  <router-view/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
