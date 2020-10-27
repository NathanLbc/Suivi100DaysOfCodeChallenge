<template>
  <div>
    <div class="menu">
      <nuxt-link to="/">
        <div class="menu-btn round-lg border">
          <div class="titre">Home</div>
        </div>
      </nuxt-link>
      <nuxt-link to="/map">
        <div class="menu-btn round-lg border">
          <div class="titre">Map</div>
        </div>
      </nuxt-link>

      <nuxt-link to="/reduce">
        <div class="menu-btn round-lg border">
          <div class="titre">Reduce</div>
        </div>
      </nuxt-link>

      <nuxt-link to="/filter">
        <div class="menu-btn round-lg border">
          <div class="titre">Filter</div>
        </div>
      </nuxt-link>

      <nuxt-link to="/async">
        <div class="menu-btn round-lg border">
          <div class="titre">Async</div>
        </div>
      </nuxt-link>

      <nuxt-link to="/promises">
        <div class="menu-btn round-lg border">
          <div class="titre">Promises</div>
        </div>
      </nuxt-link>

      <nuxt-link to="/computed">
        <div class="menu-btn round-lg border">
          <div class="titre">Computed</div>
        </div>
      </nuxt-link>
      <nuxt-link to="/asyncData">
        <div class="menu-btn round-lg border">
          <div class="titre">asyncData</div>
        </div>
      </nuxt-link>
    </div>
    <Nuxt />
  </div>
</template>

<style>
.side-menu {
  height: 15%;
  width: 15%;
  background-color: lightgrey;
}
.container {
  margin: 0 0 0 15%;
  padding-left: 2%;
  min-height: 100vh;
  justify-content: top;
  align-items: top;
  text-align: top;
  color: white;
}
.menu {
  width: 15%;
  position: fixed;
  background-color: lightgrey;
}
.titre {
  padding: 30px;
}
.menu-btn {
  font-size: 25px;
  color: lightgrey;
  background-color: #020a53;
  width: 100%;
  height: 100px;
  text-align: center;
  display: inline-block;
}
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  background-color: #08298a;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>
