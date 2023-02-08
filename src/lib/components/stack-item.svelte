<script lang="ts">
	export let iconUrl: string;
	export let label: string;
</script>

<div class="stack-item">
	<div class="icon">
		<img width="80" src={iconUrl} alt={label} />
	</div>
	<p class="label">{label}</p>
</div>

<style lang="scss">
	.stack-item {
		text-align: center;
		cursor: default;
		margin-bottom: 60px;
		display: flex;
		flex-direction: column;
		align-items: center;

		.icon,
		img {
			width: 60px;
			height: 60px;
		}

		img {
			filter: grayscale(1);
			transition: all 150ms;
			object-fit: contain;
		}

		.label {
			font-size: 14px;
			text-transform: capitalize;
			margin-top: 16px;
		}

		&:hover {
			img {
				filter: grayscale(0);
			}
		}
	}
</style>
