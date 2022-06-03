<template>
	<div>
		<main class="container">
			<div class="d-flex align-items-center">
				<HelloWorld/>
				<Header/>
			</div>

			<div>
				<Footer/>
			</div>
		</main>
	</div>
</template>

<script>

import HelloWorld from './Helloword/HelloWorld.vue';
import Header from './General/Header/Header.vue';
import Footer from './General/Footer/Footer.vue';


	export default {
		name: 'Index',

		components: {
			HelloWorld,
			Header,
			Footer,
		}
	}
</script>