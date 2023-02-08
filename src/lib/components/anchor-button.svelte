<script lang="ts">
	export let href: string;
	export let label: string;
</script>

<a class="anchor-button" {href}>{label}</a>

<style lang="scss">
	.anchor-button {
		display: inline-block;
		border: none;
		background: #000;
		color: white;
		padding: 16px 32px;
		text-decoration: none;
		flex-grow: 0;
		text-align: left;
	}
</style>
