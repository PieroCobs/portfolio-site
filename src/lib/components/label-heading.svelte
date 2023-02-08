<script lang="ts">
	export let label: string;
</script>

<span>{@html label}</span>

<style lang="scss">
	span {
		text-transform: uppercase;
		color: $color-label-heading;
		font-size: 12px;
		font-weight: 700;
	}
</style>
