<template>
	<div id="picturesProfile">
		<img :src="imageLinguage" :alt="altImageLanguage" class="bgc-image">
		<img :src="avatar" :alt="altAvatar" class="profile-image">
		<BotaoTrocaImagem @mudar-imagem="trocaImagem"/>
	</div>
</template>

<script>
	import BotaoTrocaImagem from '../BotaoTrocaImagem/BotaoTrocaImagem.vue';

	export default {
		name: 'Picture',

		components: {
			BotaoTrocaImagem,
		},

		data() {
			return {
				imageLinguage: '/image/js.jpg',
				altImageLanguage: 'Javascript language on picture with backgroun in black and other colors',
				avatar: 'https://i.ibb.co/2khHMTS/135861044-3663530760381961-1838278676959512214-n.jpg',
				altAvatar: 'Profile Image',
			}
		},

		methods: {
			trocaImagem() {
				this.avatar = 'https://i.ibb.co/4fSsr0Q/1r-WSSro-DCPjr5c-IHRH8d-Wi-Zv-H8w-Rdy9-FL.jpg';
			}
		}
	}
</script>

<style lang="scss" scoped src="./Picture.scss" />
