<template>
  <div id="app">
    <router-view/>
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
.nav_option{
  text-decoration: none;
  color: rgb(90, 90, 184);
  font-size: 20px;
}

/*Chrome 隱藏卷軸*/
body::-webkit-scrollbar {
  display: none;
}
/*IE/Edge 隱藏卷軸*/
body {
  -ms-overflow-style: none;
}
</style>
