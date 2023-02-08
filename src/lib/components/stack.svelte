<script lang="ts">
	import StackItem from './stack-item.svelte';
	import typescript from '$lib/images/stack/typescript.svg';
	import javascript from '$lib/images/stack/javascript.svg';
	import flutter from '$lib/images/stack/flutter.svg';
	import reactjs from '$lib/images/stack/reactjs.svg';
	import nextjs from '$lib/images/stack/nextjs.png';
	import dart from '$lib/images/stack/dart.png';
	import svelte from '$lib/images/stack/svelte.png';
	import html from '$lib/images/stack/html.png';
	import css from '$lib/images/stack/css.png';
	import sass from '$lib/images/stack/sass.png';
	import nodejs from '$lib/images/stack/nodejs.png';
	import go from '$lib/images/stack/go.png';

	const stacks = [
		{ label: 'typescript', iconUrl: typescript },
		{ label: 'javascript', iconUrl: javascript },
		{ label: 'flutter', iconUrl: flutter },
		{ label: 'dart', iconUrl: dart },
		{ label: 'react.js', iconUrl: reactjs },
		{ label: 'next.js', iconUrl: nextjs },
		{ label: 'svelte', iconUrl: svelte },
		{ label: 'html', iconUrl: html },
		{ label: 'css', iconUrl: css },
		{ label: 'sass', iconUrl: sass },
		{ label: 'node.js', iconUrl: nodejs },
		{ label: 'go', iconUrl: go }
	];
</script>

<section class="stack">
	<h2 class="section-title">my stack</h2>

	<div class="content">
		{#each stacks as { label, iconUrl }, i}
			<div class="col">
				<StackItem {label} {iconUrl} />
			</div>
		{/each}
	</div>
</section>

<style lang="scss">
	.stack {
		margin: $column-margin-top 0;
		border-top: 1px solid $color-border;
		padding-top: $column-margin-top;
	}

	.content {
		padding-top: 4rem;
		display: flex;
		flex-wrap: wrap;
	}

	.col {
		width: calc(100% / 3);
		flex: 0 0 auto;

		@media (min-width: 768px) {
			width: calc(100% / 4);
		}

		@media (min-width: 1200px) {
			width: calc(100% / 6);
		}
	}
</style>
