<template>
	<div>
		<div>
			<h2 class="text-3xl text-blue-500 font-semibold mb-4 pb-4 border-b-2">
				About Dad jokes
			</h2>
			<p>This is an app that displays dad jokes.</p>
		</div>
	</div>
</template>

<script>
	export default {
		head() {
			return {
				title: 'About Dad Jokes',
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
