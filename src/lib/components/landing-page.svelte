<script>
	import knoxxi from '$lib/images/clients/knoxxi.svg';
	import ayuda from '$lib/images/clients/ayuda.svg';
	import AkSurfSide from '$lib/images/clients/ak-surfside.svg';
	import hempire from '$lib/images/clients/hempire.svg';
	import sindor from '$lib/images/clients/sindor.svg';
	import instantVouchers from '$lib/images/clients/instant-vouchers.svg';
	import adeo from '$lib/images/clients/adeo.png';
	import profile from '$lib/images/profile.jpg';
	import InfoBit from './info-bit.svelte';
	import Spacer from './spacer.svelte';
	import AnchorButton from './anchor-button.svelte';
</script>

<section class="landing-page">
	<h1 class="tagline">
		Peter Sabla
		<br />Frontend Software Engineer
		<br />&amp; Flutter Developer
	</h1>

	<div class="row">
		<div class="col">
			<InfoBit
				label="profile"
				info="Creative front-end engineer with passion for designing with code. Implements complex interfaces without a loss in aesthetics or functionality."
			/>
			<Spacer height={2.5} />
			<InfoBit
				label="services"
				info="Frontend Web Development<br/>Mobile Development<br/>UI/UX Design"
			/>
			<Spacer height={2.5} />
			<InfoBit label="contact" info="rickpiero237@gmail.com<br/>+233 247 081 117" />
		</div>
		<div class="col">
			<img src={profile} alt="Peter Sabla" class="profile" />
		</div>
		<div class="col">
			<InfoBit label="years of<br/>experience" info="8" isLarge />
			<Spacer height={2.5} />
			<div>
				<InfoBit label="what are<br/>you working on?" info="" />
				<AnchorButton href="mailto:rickpiero237@gmail.com" label="Get in touch" />
			</div>
			<Spacer height={2.5} />
			<div>
				<InfoBit label="projects" info="" />
				<a class="btn-text" href="#projects">browse projects</a>
			</div>
		</div>
	</div>

	<div class="clients">
		<a href="https://ayudahub.com" target="_blank" rel="noreferrer">
			<img src={ayuda} alt="ayuda" />
		</a>
		<a href="https://ecoachsolutions.com" target="_blank" rel="noreferrer">
			<img src={adeo} alt="adeo" />
		</a>
		<a href="https://knoxxi.com" target="_blank" rel="noreferrer">
			<img src={knoxxi} alt="knoxxi" />
		</a>
		<!-- <a href="#!" target="_blank">
				<img src={AkSurfSide} alt="AkSurfSide" />
			</a> -->
		<a href="https://sindorenterprise.com" target="_blank" rel="noreferrer">
			<img src={sindor} alt="sindor" />
		</a>
		<a href="https://hempireonline.com" target="_blank" rel="noreferrer">
			<img src={hempire} alt="hempire" />
		</a>
		<a href="" target="_blank" rel="noreferrer">
			<img src={instantVouchers} alt="instantVouchers" />
		</a>
	</div>
</section>

<style lang="scss">
	.landing-page {
		.tagline {
			line-height: 1.5em;
		}

		.profile {
			max-width: 100%;
		}

		.btn-text {
			display: inline-block;
			border: 1px solid #000;
			background: none;
			color: #000;
			padding: 16px;
			text-decoration: none;
			white-space: nowrap;
			text-transform: capitalize;

			&:hover {
				background: #000;
				color: white;
			}
		}
	}

	.clients {
		display: flex;
		align-items: center;
		justify-content: center;
		margin-top: $column-margin-top;
		-ms-overflow-style: none;
		overflow-x: auto;
		&::-webkit-scrollbar {
			display: none;
		}

		a {
			&:not(:last-child) {
				margin-right: 30px;

				@media screen and (min-width: 1024px) {
					margin-right: 60px;
				}
			}
		}

		img {
			width: 80px;
			filter: brightness(0%) opacity(0.4);
			transition: all 150ms;

			&:hover {
				filter: brightness(0%) opacity(1);
			}
		}
	}

	.row {
		margin: 0 -20px;

		.col {
			padding: 20px;
			max-width: 700px;
			margin: 0 auto;
		}

		.col:nth-child(2) {
			display: none;
		}

		.col:last-child {
			@media (min-width: 570px) {
				display: flex;
				justify-content: space-between;
				flex-wrap: wrap;
				align-items: flex-end;
			}
		}

		@media (min-width: 1024px) {
			display: flex;
			flex-wrap: wrap;
			justify-content: space-between;

			.col {
				max-width: auto;
			}

			.col:nth-child(odd) {
				width: 25%;
			}
			.col:nth-child(2) {
				width: 40%;
				display: inline-block;
			}
			.col:last-child {
				text-align: right;
				display: inline-block;
			}
		}
	}
</style>
