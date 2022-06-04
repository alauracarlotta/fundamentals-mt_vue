<template>
	<div>
		<button @click="ativaOuDesativa">
			Ativar
		</button>
		<p v-show="reutlize">123 JÁ</p>
	</div>	
</template>

<script>
	export default {
		name: 'ReutilizacaoComponent',

		data() {
			return {
				reutlize: false,
			}
		},

		methods: {
			ativaOuDesativa() {
				this.reutlize = !this.reutlize;
			}
		}
	}
</script>

<style lang="scss" scoped>
	div {
		margin: 100px;

		button {
			background-color: #000;
			color: #FFF;
			font-weight: bolder;
			padding: 10px;
		}

		p {
			font-size: 2rem;
		}
	}
</style>
