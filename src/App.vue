<template> <!-- Componente root da aplicação -->

	<div> <!-- Templates do vue só podem ter um elemento root por isso, é normalmente visto divs logo após a tag template -->
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