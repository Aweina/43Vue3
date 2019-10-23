
<template>
  <div id="app">
    <div id="nav">
      <h1>问卷调查表填写</h1>

      <router-link id="xs" to="/page1" style="text-decoration: none;"><span @click="a()">点击开始填写问卷</span></router-link>
    </div>
    <router-view/>
  </div>
</template>

<script>
  export default {
    data(){
      return{

      }
    },
    methods:{
      a(){
        var a=document.getElementById("xs");
        a.style.display="none";

      }
    }
  }


</script>
<style>

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
#xs span{ background: yellow;}

</style>
