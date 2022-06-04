<template>
	<div>
		<button 
			@click="
			primeiro($event); 
			segundo($event); 
			terceiro(txt3, $event); 
			quarto(txt4, $event);
			quinto($event)"
		>
			Ativar Multiplos Eventos
		</button>
		<p>{{ multiplos_eventos }}</p>
	</div>	
</template>

<script>
	export default {
		name: 'MultiplosEventos',

		data() {
			return {
				multiplos_eventos: '',
				txt3: 'Terceirooooooooooo Evento Ativado!',
				txt4: 'QUARTO, QUARTO, QUARTO!'
			}
		},

		methods: {
			primeiro(e) {
				this.multiplos_eventos = 'Primeiro Evento Ativado!';
				console.log(e);
				console.log('primeiro');
			},

			segundo(e) {
				setTimeout(() => {
					this.multiplos_eventos = 'SEGUNDO Evento Ativado!';
					console.log(e);
					console.log('segundo');
				}, 2000)
			},

			terceiro(txt, e) {
				setTimeout(() => {
					this.multiplos_eventos = txt;
					console.log(e);
					console.log('terceiro');
				}, 5000)
			},

			quarto(txt, e) {
				setTimeout(() => {
					this.multiplos_eventos = txt;
					console.log(e);
					console.log('quarto');
				}, 9000)
			},

			quinto(e) {
				setTimeout(() => {
					this.multiplos_eventos = '';
					console.log(e);
					console.log('quinto');
				}, 11000)
			},
		}
	}
</script>

<style scoped>
	div {
		margin: 100px;
	}
</style>
