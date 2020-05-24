<template>
	<div>
		<h2 class="text-3xl text-blue-500 font-semibold mb-4 pb-4 border-b-2">
			Welcome to the best dad jokes app
		</h2>
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
