<template>
	<InputText/>
	<InputText/>
	<Submit/>
</template>

<script>
	import InputText from './Form/InputText.vue'
	import Submit from './Form/Submit.vue'
	export default {
		name: 'Form',

		components: {
			InputText,
			Submit,
		}
	}
</script>
