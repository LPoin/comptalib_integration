<template>
	<div class="layout">
		<header class="header">
			<strong>
				<g-link to="/">{{ $static.metadata.siteName }}</g-link>
			</strong>
			<nav class="nav">
				<g-link class="nav__link" to="/">Home</g-link>
				<g-link class="nav__link" to="/hero/">Hero</g-link>
				<g-link class="nav__link" to="/about/">About</g-link>
			</nav>
		</header>
		<h4>
			{{ $static.metadata.siteDescription }}
		</h4>
		<slot />
		<footer class="footer">
			<g-link class="footer__link" to="https://www.comptalib.com/">Comptalib</g-link>
			<g-link class="footer__link" to="https://gridsome.org/">Gridsome</g-link>
		</footer>
	</div>
</template>

<static-query>
query {
    metadata {
        siteName
        siteDescription
    }
}
</static-query>

<style>
body {
	font-family: -apple-system, system-ui, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue",
		Arial, sans-serif;
	margin: 0;
	padding: 0;
	line-height: 1.5;
}

.layout {
	max-width: 760px;
	margin: 0 auto;
	padding-left: 20px;
	padding-right: 20px;
}

.header {
	background-color: #42b883;
	display: flex;
	justify-content: space-between;
	align-items: center;
	margin-bottom: 20px;
	padding: 5px;
	height: 80px;
}

.nav__link {
	margin-left: 20px;
}

.footer {
	background-color: #42b883;
	padding: 5px;
	margin-top: 20px;
}
.footer a {
	margin-right: 20px;
}
</style>
