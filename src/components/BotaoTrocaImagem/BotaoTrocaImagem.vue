<template>
	<div>
		<button @click="$emit('mudarImagem')">Troca Imagem</button>
	</div>
</template>

<script>
	export default {
		name: 'BotaoTrocaImagem',

		emits: ['mudarImagem'],
	}
</script>