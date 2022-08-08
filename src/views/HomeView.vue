<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">

    <button type="submit" @click="login">Login</button>
    <button type="submit" @click="logout">logout</button>
  
   
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'HomeView',
  data() {
    return {
      email : '',
      password : ''
    }
  },
 methods: {
    login(){
       axios.get('http://localhost:3000/login',{withCredentials: true})
     
    },
    logout(){
        axios.get('http://localhost:3000/logout',{withCredentials: true})
    }
 },
}
</script>
