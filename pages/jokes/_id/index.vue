<template>
	<div>
		<nuxt-link to="/jokes">Back to jokes</nuxt-link>
		<h2>{{ joke }}</h2>
		<hr>

		<small>Joke ID: {{ $route.params.id }}</small>
	</div>
</template>

<script>
	import axios from "axios";

	export default {
		data() {
			return {
				joke: {},
			}
		},
		async asyncData ({ params }) {
			const config = {
				headers: {
					'Accept': 'application/json'
				}
			};
			try {
				const res = await axios.get(`https://icanhazdadjoke.com/j/${params.id}`, config);
				return { joke: res.data.joke };
			} catch (err) {
				console.log(err);
			}
		},
		head() {
			return {
				title: this.joke,
				meta: [
					{
						hid: 'description',
						name: 'description',
						content: 'Best place for dad jokes',
					}
				],
			};
		}

	}
</script>

<style scoped>

</style>
