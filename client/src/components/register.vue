<template>
  <div class="register">
<p>register</p>
<input type="email" name="email" placeholder="email" v-model="email"><br>
<input type="password" name="password" placeholder="password" v-model="password">
<button @click="register()">Register </button>
  </div>
</template>

<script>
import AuthenticationService from '@/services/AuthenticationService.js'
export default {
  name: "register",
data(){
return{
 email:'',   
 password:''
}
},
methods :{
    register : async function(){
    await  AuthenticationService.register({
email: this.email,
password: this.password
        })
      
    }
}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
