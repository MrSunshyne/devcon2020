<template>
  <div id="app">
    <router-view />
  </div>
</template>
<script>
export default {
  created() {
    fetch(
      "https://raw.githubusercontent.com/mscraftsman/devcon2020/master/web/app/package.json"
    )
      .then(response => response.json())
      .then(data => console.log(data));
  }
};
</script>


<style lang="scss">
* {
  margin: 0;
  padding: 0;
}

html,
body {
  width: 100%;
  height: 100%;
}

html {
  // background-image: url("./assets/concept.svg");
  background-image: url("./assets/backdrop.jpg");
  background-size: cover;
  background-position: center center;
  background-repeat: no-repeat;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
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
    &.router-link-exact-active {
      color: white;
    }
  }
}
</style>
