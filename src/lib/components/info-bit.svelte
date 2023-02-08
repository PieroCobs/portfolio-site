<script lang="ts">
	import LabelHeading from './label-heading.svelte';
	import Spacer from './spacer.svelte';

	export let label: any;
	export let info: string;
	export let isLarge: boolean = false;
</script>

<div>
	<LabelHeading {label} />
	<Spacer height={1.5} />
	<p class:isLarge class="info">{@html info}</p>
</div>

<style lang="scss">
	p {
		font-family: $font-heading, serif;
		font-size: 15px;
		line-height: 2;
		margin: 0;

		&.isLarge {
			font-size: 32px;
		}
	}
</style>
