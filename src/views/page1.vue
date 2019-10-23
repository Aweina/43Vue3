<template>
  <div class="page1">

    <p>1.请问您的性别是：</p>
    <input type="radio" name="sex" value="男" v-model="sex">男
    <input type="radio" name="sex" value="女" v-model="sex">女
    <input name="sex" type="radio" value="保密" checked v-model="sex">保密
    <!--<p><router-link to="/page2" @click="doClick()" >下一步</router-link>-->
    <p><a href="#" @click="doClick()">下一步</a>
      &nbsp;&nbsp;<a href="#" @click="doBlick()">重置</a></p>

  </div>

</template>


<script>
  export default {
    name: "Page1",
    data(){
      return {
        sex:'',
      }
    },
    methods:{
      doClick() {
        this.$store.commit("addSex",{sex:this.sex});
        this.$router.push('/page2');


      }, doBlick() {
        this.sex=""

      }
    }

  }
</script>

<style type="text/css">
  .page1{height: 300px}
  .page1 h1{ padding-top: 50px}
  a{text-decoration: none; color: darkturquoise; font-weight: bold}
</style>