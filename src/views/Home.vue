<template>
  <div class="login-page">
    <div class="card">

      <label for="email">Email</label>
      <input placeholder="example@example.com" v-model="email" class="login-input" type="email" name="email" id="email">
      
      <label for="password">Password</label>
      <input placeholder="Password" v-model="password" class="login-input" type="password" name="password" id="password">

      <button @click="logIn" class="login-btn">Login</button>

      <div v-if="error.length" class="error">Ocurrió un error: {{error}}</div>

    </div>
  </div>
</template>

<script lang="ts">

import Vue from 'vue';
export default Vue.extend(
  {
    data(){
      return {
        email: '',
        password: '',
        error: ''
      }
    },
    methods: {
      
      logIn(){
        if(!this.email || !this.password){
          this.error = "Debes proveer un email y contraseña";
          return;
        }
        this.error = "";
        alert('Lo hicimos!')
      }

    }
  }
);
</script>

<style lang="scss">
.login-page {

  .card {
    background: #f1f1f1;
    border: 1px solid #cdcdcd;
    margin: 5em auto;
    max-width: 400px;
    border-radius: 0.4em;
    padding: 1em;

    .login-input {
      display: block;
      width: 100%;
      height: 40px;
      margin-bottom: 10px;
    }

    .login-btn {
      width: 100%;
      height: 40px;
    }

    .error {
      text-align: center;
      margin: 10px 0;
      color: red;
    }
  }

}
</style>
