<template>
	<div>
		<div class="flex justify-between items-baseline border-b-2 mb-4 px-4">
			<nuxt-link to="/jokes" class="inline-block px-4 py-1 mb-4 shadow rounded text-blue-500 transition-colors duration-200 hover:bg-blue-600 hover:text-white">
				Back to jokes
			</nuxt-link>
			<small class="block mb-4">Joke ID: {{ $route.params.id }}</small>
		</div>
		<p class="text-lg px-4">{{ joke }}</p>
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
