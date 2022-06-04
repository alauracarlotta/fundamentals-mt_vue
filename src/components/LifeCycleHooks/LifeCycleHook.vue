<template>
	<h2 class="teste-hierarquia">Meu nome é: <em>{{ nome }}</em></h2>
	<MultiplosEventos/>
	<Info/>
	<Form/>
</template>

<script>
	import Info from '../Info/Info.vue';
	import Form from '../Form.vue';
	import MultiplosEventos from '../MultiplosEventos/MultiplosEventos.vue';

	export default {
		name: 'LifeCycleHook',

		components: {
			Info,
			Form,
			MultiplosEventos,
		},

		data() {
			return {
				nome: 'Ainda não sei!',
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