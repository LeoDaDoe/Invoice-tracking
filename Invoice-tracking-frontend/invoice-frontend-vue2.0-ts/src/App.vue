<template>
  <!-- <b-navbar type="dark" variant="dark">
    <b-navbar-nav>
      <b-navbar-item>
        <router-link to="/">Home</router-link>
      </b-navbar-item>
      <b-navbar-item>
        <router-link to="/about">About</router-link>
      </b-navbar-item>
    </b-navbar-nav>
  </b-navbar> -->
  <div>
    <b-navbar>
      <b-nav>
        <b-nav-item>
          <router-link to="/">Home</router-link>
        </b-nav-item>
        <b-nav-item>
          <router-link to="/about">About</router-link>
        </b-nav-item>
        <b-nav-item>
          <router-link to="/workhours">Work Hours</router-link>
        </b-nav-item>
        <b-nav-item>
          <router-link to="/manageinvoices">Manage invoices</router-link>
        </b-nav-item>
      </b-nav>
    </b-navbar>
    <router-view class="container-fluid" />
    <!-- <router-view /> -->
  </div>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
  // background-image: linear-gradient(to right, blue, yellow);
  background-color: rgb(0, 0, 68);

  a {
    font-weight: bold;
    color: #91b9c9;

    &.router-link-exact-active {
      color: white;
    }
  }
}

@media (min-width: 1366px) {
  .container {
    width: 1336px;
  }
}

@media (min-width: 1400px) {
  .container {
    width: 1450px;
  }
}

@media (min-width: 1600px) {
  .container {
    width: 1650px;
  }
}

footer {
  background-color: rgb(0, 0, 68);
}
</style>
