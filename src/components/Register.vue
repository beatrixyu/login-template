<template>
  <div id="register" class="h-full">
    <div class="border-b border-gray-200">
      <div class="pl-6 pr-6">
      <h1 class="text-xl leading-relaxed mt-12 font-bold">ICH BIN NEU HIER</h1>
      <h3 class="text-gray-400 text-xs">Jetzt Dein Kundenkonto erstellen.</h3>
      <div class="mt-5">
          <div class="flex items-center">
            <span class="inline-block align-middle h-full">
              <img src="../assets/images/blackStar.png" alt="star" class="w-5 mr-3">
            </span>
            <p class="text-xs text-gray-600 leading-8">Automatisch <strong class="text-black">Punkte</strong> für Deinen Einkauf <strong class="text-black"> Sammeln</strong></p>
          </div>
          <div class="flex items-center">
            <span><img src="../assets/images/care.png" alt="care service" class="w-5 mr-3"></span>
            <p class="text-xs text-gray-600 leading-8">Rabatte & <strong class="text-black">Gratisprodukte</strong>  erhalten</p>
          </div>
          <div class="flex items-center pb-7">
            <span><img src="../assets/images/person.png" alt="customer service" class="w-5 mr-3"></span>
            <p class="text-xs text-gray-600 leading-8"><strong class="text-black">Übersicht Deiner Bestellungen </strong>und Produkte bewerten</p></div>
      </div>
    </div>
      </div>
     <form v-on:reset="resetFields" v-on:submit.prevent="submitForm" class="mt-7 pl-6 pr-6">
       <div class="form-row border border-gray-400 mt-5">
         <div class="form-field h-10">
          <!-- <label for="first-name">First Name</label> -->
          <input class="placeholder-gray-400 h-full w-full focus:ring-1 focus:ring-purple-600 pl-4 text-xs" type="text" id="first-name" v-model.trim="fullname" placeholder="Vorname*"/>
        </div>
      </div>
      <div class="form-row border border-gray-400 mt-5">
        <div class="form-field h-10">
          <!-- <label for="email">Email</label> -->
          <input class="placeholder-gray-400 h-full w-full pl-4 text-xs" type="text" id="email" v-model.trim="email" placeholder="E-Mail Adresse*"/>
        </div>
      </div>
       <div class="form-row border border-gray-400 mt-5">
        <div class="form-field h-10">
          <!-- <label for="password">Password</label> -->
          <input class="placeholder-gray-400 h-full w-full pl-4 text-xs" type="password" id="password" v-model.trim="password" placeholder="Passwort*"/>
        </div>
      </div>
       <button class="h-11 bg-green-300 rounded-sm w-full mt-5 uppercase text-white primary font-extrabold" type="submit" v-bind:disabled="!formIsValid">registrieren</button>
     </form>              
  </div>
</template>

<script>
export default {
    name:'registerForm',
    data() {
      return {
        fullname: "",
        email: "",
        password:""
      };
    },
    computed: {
      formIsValid(){
        return this.fullname && this.email && this.password;
      }
    }
}

</script>