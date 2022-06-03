<template>
	<h1>{{ hello }}</h1>
</template>

<script>

export default {
	name: 'HelloWorld',

	data() {
		return {
			hello: 'Hello World, bitches!',
		}
	},

}
</script>

<style lang="scss" scoped src="./HelloWorld.scss" />