<template>
  <div id="main">
      <h1>ICH BIN NEU HIER</h1>
      <h3>Jetzt Dein Kundenkonto erstellen.</h3>
      <div>
          <div><span><img src="" alt=""></span><p>Automatisch Punkte für Deinen Einkauf Sammeln</p></div>
          <div><span><img src="" alt=""></span><p>Rabatte & Gratisprodukte erhalten</p></div>
          <div><span><img src="" alt=""></span><p>Übersicht Deiner Bestellungen und Produkte bewerten</p></div>
      </div>
      <p>
         <router-link to="/register">Register</router-link>
         <router-link to="/login">Go to Bar</router-link>
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
