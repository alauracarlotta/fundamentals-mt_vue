<template>
	<div id="picturesProfile">
		<img :src="imageLinguage" :alt="altImageLanguage" class="bgc-image">
		<img :src="avatar" :alt="altAvatar" class="profile-image">
	</div>
</template>

<script>
	export default {
		name: 'Picture',

		data() {
			return {
				imageLinguage: '/image/js.jpg',
				altImageLanguage: 'Javascript language on picture with backgroun in black and other colors',
				avatar: 'https://i.ibb.co/2khHMTS/135861044-3663530760381961-1838278676959512214-n.jpg',
				altAvatar: 'Profile Image',
			}
		}
	}
</script>

<style lang="scss" scoped src="./Picture.scss" />
