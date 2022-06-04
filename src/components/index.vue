<template>
	<div>
		<main class="container">
			<Header :esta_logado="true" />
			<Footer/>
		</main>
	</div>
</template>

<script>

import Header from './General/Header/Header.vue';
import Footer from './General/Footer/Footer.vue';


	export default {
		name: 'Index',

		components: {
			Header,
			Footer,
		}
	}
</script>