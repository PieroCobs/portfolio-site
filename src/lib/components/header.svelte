<script>
	import Social from './social.svelte';
</script>

<header class="header">
	<nav>
		<a href="#projects">works</a>
		<a href="#contact">contact</a>
	</nav>

	<Social />
</header>

<style lang="scss">
	.header {
		display: flex;
		justify-content: space-between;
		padding: calc($column-margin-top / 2) 0 0;

		nav {
			display: flex;

			a {
				display: flex;
				height: 100%;
				align-items: center;
				padding: 0 0.5rem;
				color: $color-text;
				font-weight: 700;
				font-size: 0.7rem;
				text-transform: uppercase;
				letter-spacing: 0.1em;
				transition: color 0.2s linear;
			}
		}
	}
</style>
