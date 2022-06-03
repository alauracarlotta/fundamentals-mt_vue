<template>
	<div>
		<Index/>
		<LifeCycleHook />
		<!-- <p>{{ testando }}</p> -->
	</div>
</template>

<script>
import Index from './components/index.vue';
import LifeCycleHook from './components/LifeCycleHooks/LifeCycleHook.vue';

export default {
	name: 'App',
	
	components:{
		Index,
		LifeCycleHook
	},

	data() {
		return {
			testando: 'Teste de componente (app também é um componente) ',
		}
	}
}
</script>