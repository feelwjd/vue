<template>
<div>
   <div id="nav">
      <router-link to="/"><font size= "14px"> Home </font></router-link>
      <router-link to="/about"><font size= "14px"> About </font></router-link>
      <router-link to="/exercise1"><font size= "14px"> 실습 1 </font></router-link>
      <router-link to="/exercise2"><font size= "14px"> 실습 2 </font></router-link>
      <router-link to="/exercise3"><font size= "14px"> 실습 3 </font></router-link>
      <router-link to="/Minjeongpil"><font size= "14px"> 민정필 </font></router-link>              </div>
  <router-view />
</div>
</template>

<script>
export default {
  name: 'App',
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>