<template>
  <div id="app">
    <b-navbar toggleable type="inverse" variant="primary">
      <b-nav-toggle target="nav_collapse"></b-nav-toggle>
      <b-link class="navbar-brand" to="/">
        <img src="../static/img/inexor-logo.svg" style="width: 50px; height: 58px;">
        <span>Inexor Flex</span>
      </b-link>
      <b-collapse is-nav id="nav_collapse">
        <b-nav is-nav-bar>
          <b-nav-item></b-nav-item>
          <b-nav-item v-for="item in navItems" :to="item.route" :key="item.label">{{item.label}}</b-nav-item>
        </b-nav>
      </b-collapse>
    </b-navbar>
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'app',
  data: () => ({
    navItems: [
      {
        route: '/profiles',
        label: 'Profiles',
      },
      {
        route: '/instances',
        label: 'Instances',
      },
      {
        route: '/media',
        label: 'Media',
      },
      {
        route: '/interfaces',
        label: 'Interfaces',
      },
      {
        route: '/releases',
        label: 'Releases',
      },
      {
        route: '/logging',
        label: 'Logging',
      },
      {
        route: '/info',
        label: 'Information',
      },
    ],
  }),
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 0px;
}

ul:not(.md-list) > li + li {
  margin-top: 0px;
}

/*
.md-list > li, li {
  margin-top: 0px;
}
*/

.btn-circle {
  width: 30px;
  height: 30px;
  text-align: center;
  padding: 6px 0;
  font-size: 12px;
  line-height: 1.428571429;
  border-radius: 15px;
}
.btn-circle.btn-lg {
  width: 50px;
  height: 50px;
  padding: 10px 16px;
  font-size: 18px;
  line-height: 1.33;
  border-radius: 25px;
}
.btn-circle.btn-xl {
  width: 70px;
  height: 70px;
  padding: 10px 16px;
  font-size: 24px;
  line-height: 1.33;
  border-radius: 35px;
}

.btn-circle.btn-xxl {
  width: 120px;
  height: 120px;
  padding: 10px 16px;
  font-size: 36px;
  line-height: 1.33;
  border-radius: 60px;
}

.navbar-default .navbar-nav > .active{
  color: #000;
  background: #ff0000;
}
.navbar-default .navbar-nav > .active > a,
.navbar-default .navbar-nav > .active > a:hover,
.navbar-default .navbar-nav > .active > a:focus {
  color: #000;
  background: #d65c14;
}

</style>
