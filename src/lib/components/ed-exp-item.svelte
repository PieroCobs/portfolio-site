<script lang="ts">
	export let title: string;
	export let institution: string;
	export let url: string;
	export let duration: string;
</script>

<div class="ed-exp">
	<h3 class="title">{@html title}</h3>
	<a href={url} target="_blank" rel="noreferrer">
		<span class="subtext institution">{institution}</span>
	</a>
	<span class="subtext duration">{duration}</span>
</div>

<style lang="scss">
	.ed-exp {
		width: 100%;

		.title {
			text-transform: capitalize;
			margin-bottom: 8px;
			line-height: 1.5;
		}

		.subtext {
			font-size: 12px;
			color: $color-label-heading;
			text-transform: capitalize;
			display: block;

			&:last-child {
				margin-top: 8px;
			}
		}
	}
</style>
