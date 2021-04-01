<template>
  <div id="app">
    
    <router-view/>
  </div>
</template>

<style lang="scss">
*{
  padding: 0;
  margin: 0;
}
#app{
  min-height: 100vh;
  background-image: url('http://localhost:8080/assets/background.jpg');
  background-position: bottom;
}
</style>
