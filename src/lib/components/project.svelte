<script lang="ts">
	import Spacer from './spacer.svelte';

	export let name: string, thumb: string, roles: string, url: string;
</script>

<div class="project">
	<a href={url} target="_blank" rel="noreferrer">
		<div class="thumb">
			<img src={thumb} alt={name} />
		</div>
		<Spacer height={1} heightSm={0.3} />
		<span class="roles">{roles}</span>
		<h4 class="name">{name}</h4>
	</a>
</div>

<style lang="scss">
	.project {
		width: 100%;

		a {
			text-decoration: none;
		}

		.thumb {
			background: #0001;
		}

		.thumb,
		img {
			width: 100%;
			aspect-ratio: 4 / 3;
		}

		img {
			object-fit: fill;
			/* filter: grayscale(1); */
		}

		img,
		.name {
			transition: all 200ms;
		}

		.roles {
			font-size: 12px;
			text-transform: capitalize;
			color: $color-label-heading;
		}

		.name {
			text-transform: capitalize;
			/* font-family: $font-body, sans-serif; */
			font-size: 20px;
			font-weight: 400;
			margin: 8px 0 0;
			opacity: 0.5;
		}

		&:hover {
			img {
				filter: grayscale(0);
			}
			.name {
				opacity: 1;
			}
		}
	}
</style>
