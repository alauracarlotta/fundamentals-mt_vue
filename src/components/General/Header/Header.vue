<template>
	<div class="d-flex align-items-center">
		<HelloWorld/>	
		<nav>
			<ul class="d-flex justify-content-start">
				<a v-for="items in menu" :key="items" href="#"><li class="px-5">{{ items }}</li></a>
			</ul>
		</nav>
	</div>
</template>

<script>
import HelloWorld from '../../Helloword/HelloWorld.vue';

	export default {
		name: 'Header',

		components: {
			HelloWorld,
		},

		data() {
			return {
				menu: ['Home', 'Hamburguers', 'Sucos', 'Porções'],
			}
		}
	}
</script>

<style lang="scss" src="./Header.scss" />
