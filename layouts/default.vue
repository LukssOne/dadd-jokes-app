<template>
	<div class="antialiased text-gray-900">
		<AppHeader/>
		<div class="max-w-5xl mx-auto pt-8">
			<nuxt />
		</div>
	</div>
</template>

<script>
	import AppHeader from "../components/AppHeader";

	export default {
		components: {
			AppHeader
		}
	}
</script>
