<template>
	<div class="antialiased text-gray-900">
		<AppHeader/>
		<div class="max-w-5xl mx-auto pt-8">
			<nuxt />
		</div>
	</div>
</template>

<script>
	// TODO: Create VUEX Data
	// TODO: Create Client for API
	// TODO: Create Error page
	// TODO: Create Transitions
	// TODO: Create loading
	// TODO: Extract CSS separately
	import AppHeader from "../components/AppHeader";

	export default {
		components: {
			AppHeader
		}
	}
</script>
