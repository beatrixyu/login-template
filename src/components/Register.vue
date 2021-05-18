<template>
  <div id="login">
    <h1>Register</h1>
     <form v-on:reset="resetFields" v-on:submit.prevent="submitForm" class="border-4">
       <div class="form-row border-2">
         <div class="form-field">
          <!-- <label for="first-name">First Name</label> -->
          <input type="text" id="first-name" v-model.trim="fullname" placeholder="Vorname*"/>
        </div>
      </div>
      <div class="form-row border-2">
        <div class="form-field">
          <!-- <label for="email">Email</label> -->
          <input type="text" id="email" v-model.trim="email" placeholder="E-Mail Adresse*"/>
        </div>
      </div>
       <div class="form-row border-2">
        <div class="form-field">
          <!-- <label for="password">Password</label> -->
          <input type="password" id="password" v-model.trim="password" placeholder="Passwort*"/>
        </div>
      </div>
       <button type="submit" v-bind:disabled="!formIsValid">registrieren</button>
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