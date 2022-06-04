<template>
	<div>
		<Picture/>
		<p v-if="isWorking">Estou trabalhando no momento;</p>
		<p v-else>Estou em busca de novas oportunidades, posso iniciar imediatamente;</p>
		<h1>Tenho a expriência de 1 ano como dev front-end;</h1>
		<p>Trabalhei com liguagens no front-end: </p>
		<ul>
			<li v-for="(linguagem, index) in frontEnd" :key="index">{{ linguagem }}</li> 
		</ul>

		<p>Trabalhei com liguagens no back-end: </p>
		<ul>
			<!-- <li v-for="item in backEnd" :key="item"> ou -->
			<li v-for="item in backEnd" :key="item.id">
				{{ item.lang }} - {{ item.experience }} 
				<span v-if="item.experience > 1">anos.</span> 
				<span v-else>ano.</span>
			</li>
		</ul>
		<p class="teste">Usei como ferramentas também: Linux ubuntu e git.</p>

		<p v-if="1 > 2">Teste 1</p>
		<p v-if="4 > 2">Teste 2</p>

		<p v-show="showEmail">Mande um email para: {{ email }} </p> <!-- Mostra ou não mostra, não há um 'v-show-else'. Geralmente usado para botões checkbox -->
		
		<p class="emailSecondary">emailSecondary: {{ userEmailProps  }}</p>

		<p v-show="showPhone">Mande um email para: {{ phone }} </p>
		<div>
			<button @click="phoneNumber">{{ textoBotao }}</button>
		</div>

		<p>Para acessar o meu portifolio, <a v-bind:href="link" target="blank" rel="noreferrer noopener">basta clicar aqui</a></p>
	
		<p class="pets">Eu seu mãe de uma {{ petType }}, a {{ petName }}!</p>
	</div>
</template>

<script>
	import Picture from '../Picture/Picture.vue';

	export default {
		name: 'Info',

		components: {
			Picture,
		},

		props: {
			petName: String,
			petType: String,
			userEmailProps: String,
			isWorking: Boolean
		},

		data() {
			return {
				showEmail: true,
				showPhone: false,
				email: 'laura@gmail.com',
				phone: '(11) 98758-8455',
				link: 'https://www.linkedin.com/in/lauracarlotta/',
				textoBotao: 'Mostra phone',
				frontEnd: [
					'Javascript',
					'jQuery',
					'HTML',
					'CSS'
				],
				backEnd: [
					{
						id: 1,
						lang: 'Python',
						experience: 2
					},
					{
						id: 2,
						lang: 'PHP',
						experience: 1
					},
					{
						id: 3,
						lang: '.NET',
						experience: 4
					},
				]
			}
		},

		methods: {
			phoneNumber() {
				this.showPhone = !this.showPhone;

				if(!this.showPhone) {
					this.textoBotao = 'Mostra phone';
				} else {
					this.textoBotao = 'Esconde phone';
				}
			}
		}
	}
</script>

<style lang="scss" scoped>
	div {
		p.pets,
		p.emailSecondary {
			font-size: 3rem;
		}
	}
</style>
