<script>
	import Nav from '../components/Nav.svelte';
</script>

<style type='text/scss'>
@import "../styles/theme.scss";
	main {
		background-color: $alt-color;
	}

	@media (min-width: 959px) {
		main {
			position: relative;
			margin: 0 0 0 250px;
			box-sizing: border-box;
		}
	}
</style>

<Nav />

<main >
	<slot></slot>
</main>