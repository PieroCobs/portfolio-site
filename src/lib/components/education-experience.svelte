<script>
	import EdExpItem from './ed-exp-item.svelte';
	import LabelHeading from './label-heading.svelte';
	import Spacer from './spacer.svelte';
</script>

<section class="ene">
	<h2 class="section-title">experience</h2>

	<div class="content">
		<!-- <div class="col-1">
			<Spacer height={2} />
			<LabelHeading label="education" />
			<Spacer height={2} />

			<EdExpItem
				title="BA<br/>Communication Studies"
				institution="African University College of Communication"
				url="https://aucc.edu.gh/"
				duration="2017 - 2021"
			/>
			<Spacer height={1} />
			<EdExpItem
				title="Diploma<br/>Software Engineering"
				institution="IPMC College of Technology"
				url="https://ipmctraining.com/"
				duration="2013 - 2015"
			/>
			<Spacer height={1} />
			<EdExpItem
				title="Nanodegree<br/>AWS machine learning<br/>foundations"
				institution="udacity"
				url="https://graduation.udacity.com/confirm/VLXTUCLG"
				duration="october 2021"
			/>
		</div> -->
		<div class="col-1">
			<Spacer height={2} />
			<div class="row">
				<div class="col">
					<EdExpItem
						title="mobile developer & frontend developer"
						institution="SmartSapp"
						url="https://smartsapp.com/"
						duration="january 2024 - december 2024"
					/>
					<Spacer height={1} />
					<EdExpItem
						title="product manager"
						institution="ayudahub"
						url="https://ayudahub.com/"
						duration="september 2023 - December 2023"
					/>
					<Spacer height={1} />
					<EdExpItem
						title="frontend engineer"
						institution="ayudahub"
						url="https://ayudahub.com/"
						duration="june 2022 - august 2023"
					/>
				</div>
			</div>
		</div>
		<div class="col-2">
			<!-- <Spacer height={2} />
			<LabelHeading label="experience" /> -->
			<Spacer height={2} />

			<div class="row">
				<div class="col">
					<EdExpItem
						title="flutter developer"
						institution="ecoach"
						url="https://ecoachsolutions.comm"
						duration="october 2021 - june 2022"
					/>
					<Spacer height={1} />
					<EdExpItem
						title="frontend developer &<br/>UI/UX designer"
						institution="ayudahub"
						url="https://ayudahub.com/"
						duration="december 2018 - september 2021"
					/>
					<Spacer height={1} />
					<EdExpItem
						title="projects associate"
						institution="kumasi hive"
						url="https://kumasihive.com"
						duration="june 2018 - november 2018"
					/>
				</div>
			</div>
		</div>
	</div>
</section>

<style lang="scss">
	.ene {
		margin: $column-margin-top 0;
		border-top: 1px solid $color-border;
		padding-top: $column-margin-top;
	}

	.content {
		padding-top: 1rem;
		display: flex;
		flex-wrap: wrap;
	}

	.col-1,
	.col-2 {
		width: 100%;
		flex: 0 0 auto;
	}

	@media (min-width: 768px) {
		.col-1,
		.col-2 {
			width: calc(100% / 2);
		}

		.col-1 {
			padding-right: 40px;
		}
	}

	@media (min-width: 1200px) {
		.col-1 {
			width: calc(100% / 2);
		}

		.col-2 {
			width: calc(100% * 0.5);

			.row {
				display: flex;
			}

			.col {
				width: calc(100% / 2);
			}
		}
	}
</style>
