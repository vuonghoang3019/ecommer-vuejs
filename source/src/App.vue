<template>
  <div class="d-flex flex-column flex-md-row align-items-center p-3 px-md-4 mb-3 bg-white">
    <h5 class="my-0 mr-md-auto font-weight-normal">Vue mini project</h5>
    <nav class="my-2 my-md-0 mr-md-3">
      <a href="#" class="p-2 text-dark">Product manager</a>
      <a href="#" class="p-2 text-dark">User manager</a>
    </nav>
    <a href="" routerlink="cart"></a>
  </div>
  
  <div class="pricing-header px-3 py-3 pt-md-5 pb-md-4">
    <h2 class="display-4">Product Management</h2>
    <p><a href="">Add new</a></p>
  </div>

  <div class="container">
    <div class="card-deck mb-3 text-center">
      <table class="table table bordered">
        <thead>
          <tr>
            <th scope="col">#</th>
            <th scope="col">Product Name</th>
            <th scope="col">Price</th>
            <th scope="col">Handle</th>
          </tr>
        </thead>
      </table>
    </div>
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
