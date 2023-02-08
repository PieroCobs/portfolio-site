<script>
	import '/static/styles/index.css';
	import Header from '$lib/components/header.svelte';
	import Footer from '$lib/components/footer.svelte';
</script>

<div>
	<div class="container">
		<Header />

		<main>
			<slot />
		</main>

		<Footer />
	</div>
</div>
