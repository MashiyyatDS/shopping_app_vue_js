<template>
  <div class="navbars sticky-top">
      <nav class="navbar navbar-expand-lg navbar navbar-dark bg-dark">
          <div class="container-fluid container">
            <a class="navbar-brand" href="/">Shopping App</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
              <i class="fa fa-bars"></i>
            </button>
            <div class="collapse navbar-collapse justify-content-end" id="navbarSupportedContent">
              <ul v-if="authenticated" class="navbar-nav mb-2 mb-lg-0">
                <li class="nav-item d-flex justify-content-center">
                  <a class="nav-link" href="/products">Products</a>
                </li>
                <li v-if="authenticated" class="nav-item d-flex justify-content-center">
                  <a class="nav-link" href="profile">Mashiyyat</a>
                </li>
                <li class="nav-item d-flex justify-content-center">
                  <a class="nav-link" href="#">Logout</a>
                </li>
              </ul>
              <ul v-else class="navbar-nav mb-2 mb-lg-0">
                <li class="nav-item d-flex justify-content-center">
                  <a class="nav-link" href="/products">Products</a>
                </li>
                <li class="nav-item d-flex justify-content-center">
                  <a class="nav-link" href="/login">Login</a>
                </li>
                <li class="nav-item d-flex justify-content-center">
                  <a class="nav-link" href="#">Register</a>
                </li>
              </ul>
            </div>
          </div>
      </nav>
      <nav class="navbar navbar-expand-lg navbar-light bg-light mb-5">
          <div class="container center">
              <div class="col-md-6">
                <form action="/search/">
                    <div class="input-group">
                      <input type="text" class="form-control" placeholder="Search product">
                      <button class="btn btn-outline-primary"><i class="fa fa-search"></i></button>
                    </div>
                </form>
              </div>
              <div class="col-md-6 d-flex justify-content-end">
                <a href="/products" class="btn btn-outline-dark m-1">
                  <i class="fa fa-shopping-cart"></i>
                </a>
                <a href="/products" class="btn btn-outline-dark m-1">
                  Buy now
                </a>
              </div>
          </div>
      </nav>
  </div>
</template>

<script>

  export default {
    name: 'Navbar',
    data() {
      return {
        authenticated: true
      }
    }
  }

</script>

<style scoped>

</style>