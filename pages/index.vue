<template>
	<div>
		<h2 class="text-3xl text-blue-500 font-semibold mb-4 pb-4 border-b-2">
			Welcome to the best dad jokes app
		</h2>
		<nuxt-link to="/jokes" class="bg-blue-600 block duration-200 hover:bg-blue-800 inline-block px-8 py-2 rounded-lg font-semibold text-lg text-white transition-colors mb-4">Go to Jokes</nuxt-link>
	</div>
</template>

<script>
	export default {
		head() {
			return {
				title: 'Welcome To Dad Jokes',
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
