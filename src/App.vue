<template>
	<div>
		<Index/>
		<!-- <p>{{ testando }}</p> -->
	</div>
</template>

<script>
import Index from './components/index.vue';

export default {
	name: 'App',
	
	components:{
		Index,
	},

	data() {
		return {
			testando: 'Teste de componente (app também é um componente) ',
		}
	}
}
</script>