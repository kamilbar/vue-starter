<template>
<!--
  <div>
	<div v-if="email.length < 10">Ale masz krótki adres!</div>
	<div v-else-if="email.length < 15">Twój adres e-mail jest w sam raz.</div>
	<div v-else>Twój adres e-mail jest stanowczo za długi.</div>
	<div>Dlugosc twojego maila: {{ email.length }}</div>
	<h1>Twój e-mail: {{ email }}. </h1>
	<input type="email" v-model="email">
	<button @click="alertMyEmail()">Wyświetl mój e-mail w alercie</button>
  </div>
-->
  <div v-if="authenticated">
	Witaj {{ email }}!
	<br><br>
	<a @click="logOut">Wyloguj</a>
  </div>
  <div v-else>
	<h1> Witaj w systemie do zapisów na zajęcia</h1>
	Zaloguj się e-mailem 
	<input type="email" v-model="email">
	<button @click="logIn">Wchodzę</button>
  </div>
</template>

<script>
import "milligram";

export default {
	data() {
	  return {
		authenticated: false,
		email: 'Twój email',
		password: ''
	  };
	},
	methods: {
//		alertMyEmail() {
//			alert(this.email);
//		},
		
		logIn() {
			this.authenticated = true;
		},
		logOut(){
			this.authenticated = false;
			this.email = "";
		}
	}
}
</script>

<style>
	a{
		color: green;
	}
	a:hover{
		color: red;
		text-decoration: underline;
	}
</style>
