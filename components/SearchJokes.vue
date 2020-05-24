<template>
	<form @submit.prevent="onSubmit" class="flex">
		<input type="text" v-model="text" placeholder="Search jokes..." class="form-input h-10">
		<input type="submit" value="Search Jokes" class="bg-blue-600 block cursor-pointer duration-200 h-10 hover:bg-blue-800 inline-block px-6 rounded-r text-white transition-colors">
	</form>
</template>

<script>
	export default {
		name: "SearchJokes",
		data() {
			return {
				text: '',
			}
		},
		methods: {
			onSubmit() {
				this.$emit('search-text', this.text);
				this.text = '';
			}
		}
	}
</script>
