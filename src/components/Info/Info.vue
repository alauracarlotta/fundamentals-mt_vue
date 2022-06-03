<template>
	<div>
		<p v-if="isWorking">Estou trabalhando no momento;</p>
		<p v-else>Estou em busca de novas oportunidades, posso iniciar imediatamente;</p>
		<p>Tenho a expriência de 1 ano como dev front-end;</p>
		<p>Trabalhei com liguagens: JS, HTM e CSS;</p>
		<p>Usei como ferramentas também: Linux ubuntu e git.</p>

		<p v-if="1 > 2">Teste 1</p>
		<p v-if="4 > 2">Teste 2</p>

		<p v-show="showEmail">Mande um email para: {{ email }} </p> <!-- Mostra ou não mostra, não há um 'v-show-else'. Geralmente usado para botões checkbox -->
	</div>
</template>

<script>
	export default {
		name: 'Info',

		data() {
			return {
				isWorking: false,
				showEmail: true,
				email: 'laura@gmail.com'
			}
		},
	}
</script>
