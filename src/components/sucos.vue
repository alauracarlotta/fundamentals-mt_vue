<template>
	<div>
		<main class="container">
			<Header/>
			<Footer/>
		</main>
	</div>
</template>

<script>

import Header from './General/Header/Header.vue';
import Footer from './General/Footer/Footer.vue';


	export default {
		name: 'sucos',

		components: {
			Header,
			Footer,
		}
	}
</script>