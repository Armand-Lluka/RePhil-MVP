<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/user">User</router-link>

    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
#app {
  @import url('https://fonts.googleapis.com/css?family=Rubik|Signika&display=swap');
  font-family: 'Signika', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;
    text-align: left;
    padding: 5px;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
