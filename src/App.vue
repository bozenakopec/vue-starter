<template>
  <div>

  <h1> Witaj w systemie do zapisz się na zajęcia! {{ email }}</h1>
  <div v-if="!isAutenticated">
  Zaloguj się e-mailem
<input type = "text" v-model = "email">

<button @click = "LogIn()"> Zaloguj  się </button>

</div>
<div v-else>
<h2> Witaj {{ email }} </h2>
<a @click="LogOut()" >Wyloguj </a>

 </div>

	</div>
</template>

<script>
import "milligram";


export default {
data() {
  return {
    email: '',
    password: '',
	isAutenticated: false
  };
},
methods: {
LogIn(){
this.isAutenticated=true
},
LogOut() {
this.isAutenticated=false;
}
}
 
}
</script>

<style>

</style>
