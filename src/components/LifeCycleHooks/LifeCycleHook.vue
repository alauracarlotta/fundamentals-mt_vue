<template>
	<h2>Meu nome é: <em>{{ nome }}</em></h2>
	<Info/>
	<Form/>
</template>

<script>
	import Info from '../Info/Info.vue';
	import Form from '../Form.vue';

	export default {
		name: 'LifeCycleHook',

		components: {
			Info,
			Form
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