<template>
	<div class="d-flex align-items-center">
		<HelloWorld/>	
		<nav>
			<ul class="d-flex justify-content-start">
				<a v-for="items in menu" :key="items" href="#">
					<li class="px-5">
						{{ items }}
					</li>
				</a>

				<a v-if="esta_logado" href="">
					<li>Perfil</li>
				</a>

				<!-- <a v-if="logginOn">
					<li>
						<a href="">Meu perfil</a>
					</li>
					<li v-for="itemsLoggin in logginOn" :key="itemsLoggin"><a href="">{{ itemsLoggin }}</a></li>
					
					<a v-if="logginOn && settings">
					<li v-for="itemsLoggin in $props[itemsLoggin]" :key="itemsLoggin">
						{{ itemsLoggin }}
					</li>
					<li v-for="itemsLoggin in $props[0]" :key="itemsLoggin[1].itemLogado">
						{{ itemsLoggin }}
					</li>
				</a> -->
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

		props: ['esta_logado'],

		/* props: {
			logginOn: Boolean
			// logginOn: [],
		}, */

		/* props: [
			"logginOn",
			"settings",
			[
				{
					itemLogado: "settings"
				},
				{
					itemLogado: "meu perfil"
				},
				{
					itemLogado: "sair"
				},
			]
		], */

		data() {
			return {
				menu: ['Home', 'Hamburguers', 'Sucos', 'Porções'],
				// logginOn: ['Meu perfil', 'settings', 'loggout']
			}
		}
	}
</script>

<style lang="scss" src="./Header.scss" />
