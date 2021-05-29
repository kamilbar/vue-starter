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
  <div>
	<h1> Witaj w systemie do zapisów na zajęcia</h1>
	Zaloguj się e-mailem 
	<input type="email" v-model="email">
	<button>Wchodzę</button>
  </div>
</template>

<script>

export default {
	data() {
	  return {
		email: 'Twój email',
		password: ''
	  };
	},
	methods: {
		alertMyEmail() {
			alert(this.email);
		}
	}
}
</script>

<style>

</style>
