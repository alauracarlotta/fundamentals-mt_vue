<template>
	<nav>
		<ul class="d-flex justify-content-start">
			<a v-for="items in menu" :key="items" href="#"><li class="px-5">{{ items }}</li></a>
		</ul>
	</nav>
</template>

<script>
	export default {
		name: 'Header',

		data() {
			return {
				menu: ['Home', 'Hamburguers', 'Sucos', 'Porções'],
			}
		}
	}
</script>

<style lang="scss" src="./Header.scss" />
