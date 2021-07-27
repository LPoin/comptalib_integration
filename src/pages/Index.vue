<template>
	<Layout>
		<!-- Learn how to use images here: https://gridsome.org/docs/images -->
		<g-image alt="Example image" src="~/favicon.png" width="135" />

		<h1>Welcome home !</h1>

		<p>
			Welcome on my Comptalib test with Gridsome ! <br />
			It's a pretty cool framework and whatever happens, I didn't waste my time :)
		</p>
	</Layout>
</template>

<script>
export default {
	metaInfo: {
		title: "Hello, world!",
	},
};
</script>

<style>
.home-links a {
	margin-right: 1rem;
}
h1 {
	text-align: center;
}
</style>
