<template>
  <div id="main">
      
      <p>
         <router-link to="/register">Register</router-link>
         <router-link to="/login">Login</router-link>
      </p>
      <router-view></router-view>
    <Register/>
    <Login />
  </div>
</template>

<script>
import Register from './Login.vue'
import Login from './Register.vue'


export default {
  name: 'Main',
  components: {
    Register,
    Login
  }
}
</script>

<style>
   /* #main h1{
       position: absolute;
       width: 153px;
       height: 25px;
       left: 21px;
       top: 189px;
       font-family: Brandon Text;
       font-style: normal;
       font-weight: bold;
       font-size: 18px;
       line-height: 25px;
   } */
</style>
