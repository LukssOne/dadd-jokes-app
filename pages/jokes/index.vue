<template>
	<div>
		<div class="flex items-center justify-between mb-4 border-b-2 ">
			<h2 class="text-3xl text-blue-500 font-semibold mb-4">
				Dad Jokes List
			</h2>
			<SearchJokes v-on:search-text="searchText" class="mb-4" />
		</div>
		<Joke v-for="joke in jokes"
		      :key="joke.id"
		      :id="joke.id"
		      :joke="joke.joke"
		      class="block duration-200 hover:bg-blue-700 hover:scale-105 hover:text-white mb-4 px-8 py-4 rounded-lg shadow transform transition-all"
		/>
	</div>
</template>

<script>
	import axios from "axios";
	import Joke from "../../components/Joke";
	import SearchJokes from "../../components/SearchJokes";

	export default {
		components: {
			Joke,
			SearchJokes
		},
		data() {
			return {
				jokes: []
			}
		},
		async asyncData ({ params }) {
			const config = {
				headers: {
					'Accept': 'application/json'
				}
			};
			try {
				const res = await axios.get('https://icanhazdadjoke.com/search', config);
				return { jokes: res.data.results };
			} catch (err) {
				console.log(err);
			}
		},
		methods: {
			async searchText(text) {
				const config = {
					headers: {
						'Accept': 'application/json'
					}
				};

				try {
					const res = await axios.get(`https://icanhazdadjoke.com/search?term=${text}`, config);
					this.jokes = res.data.results;
				} catch (err) {
					console.log(err);
				}
			}
		},
		head() {
			return {
				title: 'Dad Jokes',
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
