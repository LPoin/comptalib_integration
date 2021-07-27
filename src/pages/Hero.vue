<template>
	<Layout>
		<div class="center">
			<h1>This is an animated hero from Lottie</h1>

			<lottie-player
				class="center"
				src="https://assets8.lottiefiles.com/packages/lf20_iorpbol0.json"
				background="transparent"
				speed="1"
				style="width: 300px; height: 300px;"
				loop
				autoplay
			></lottie-player>
		</div>
	</Layout>
</template>

<script>
export default {};
</script>

<style scoped>
.center {
	text-align: center;
	margin: auto;
}
</style>
