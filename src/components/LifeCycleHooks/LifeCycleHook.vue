<template>
	<h2 class="teste-hierarquia">Meu nome é: <em>{{ nome }}</em></h2>
	<MultiplosEventos />
	<ReutilizacaoComponent />
	<Info petType="catchorinha" petName="Maggiezinha" :userEmailProps="userEmail" :isWorking="false" />
	<Form/>
</template>

<script>
	import Info from '../Info/Info.vue';
	import Form from '../Form.vue';
	import MultiplosEventos from '../MultiplosEventos/MultiplosEventos.vue';
	import ReutilizacaoComponent from '../ReutilizacaoComponent/ReutilizacaoComponent.vue';
	
	export default {
		name: 'LifeCycleHook',

		components: {
			Info,
			Form,
			MultiplosEventos,
			ReutilizacaoComponent,
		},

		data() {
			return {
				nome: 'Ainda não sei!',
				userEmail: 'carlottattoo@gmail.com'
			}
		},

		methods: {
			lifeCycleTestMethods() {
				console.log('Executei');
			}
		},

		created() {
			setTimeout(() => {
				this.nome = 'Laura';
				this.lifeCycleTestMethods();
			}, 1000);
		},

		mounted() {
			setTimeout(() => {
				this.nome = 'Carlota';
				this.lifeCycleTestMethods();
			}, 2000);
		}
	}
</script>

<style>
.teste-hierarquia {
	color: #FF0
}
</style>