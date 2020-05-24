<template>
	<header class="bg-gray-800 flex items-center justify-between p-4 text-white">
		<h1 class="text-3xl font-semibold">Dad Jokes</h1>
		<ul class="flex">
			<li class="transition-colors duration-200 hover:bg-blue-700 rounded-lg">
				<nuxt-link class="px-4 py-1 block" to="/">Home</nuxt-link>
			</li>
			<li class="transition-colors duration-200 hover:bg-blue-700 rounded-lg">
				<nuxt-link class="px-4 py-1 block" to="/jokes">Jokes</nuxt-link>
			</li>
			<li class="transition-colors duration-200 hover:bg-blue-700 rounded-lg">
				<nuxt-link class="px-4 py-1 block" to="/about">About</nuxt-link>
			</li>
		</ul>
	</header>
</template>

<script>
	export default {
		name: "AppHeader"
	}
</script>
