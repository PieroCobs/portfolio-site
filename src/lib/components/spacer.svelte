<script lang="ts">
	import { onMount } from 'svelte';

	export let width = 0;
	export let height = 0;
	export let heightSm = 0;

	let computedHeight = height;

	onMount(() => {
		const mql = window.matchMedia('(max-width: 768px)');

		// Set initial height
		computedHeight = mql.matches ? heightSm : height;

		// Listen for changes
		const listener = (e: MediaQueryListEvent) => {
			computedHeight = e.matches ? heightSm : height;
		};

		mql.addEventListener('change', listener);

		return () => mql.removeEventListener('change', listener);
	});
</script>

<div class="spacer" style="width: {width}rem; height: {computedHeight}rem;" />
