<template>
	<div>
		<Picture/>
		<p v-if="isWorking">Estou trabalhando no momento;</p>
		<p v-else>Estou em busca de novas oportunidades, posso iniciar imediatamente;</p>
		<p>Tenho a expriência de 1 ano como dev front-end;</p>
		<p>Trabalhei com liguagens: JS, HTM e CSS;</p>
		<p>Usei como ferramentas também: Linux ubuntu e git.</p>

		<p v-if="1 > 2">Teste 1</p>
		<p v-if="4 > 2">Teste 2</p>

		<p v-show="showEmail">Mande um email para: {{ email }} </p> <!-- Mostra ou não mostra, não há um 'v-show-else'. Geralmente usado para botões checkbox -->
		
		<p v-show="showPhone">Mande um email para: {{ phone }} </p>
		<div>
			<button @click="phoneNumber">Mostra Telefone</button>
		</div>

		<p>Para acessar o meu portifolio, <a v-bind:href="link" target="blank" rel="noreferrer noopener">basta clicar aqui</a></p>
	</div>
</template>

<script>
	import Picture from '../Picture/Picture.vue';

	export default {
		name: 'Info',

		components: {
			Picture,
		},

		data() {
			return {
				isWorking: false,
				showEmail: true,
				showPhone: true,
				email: 'laura@gmail.com',
				phone: '(11) 98758-8455',
				link: 'https://www.linkedin.com/in/lauracarlotta/'
			}
		},
	}
</script>
