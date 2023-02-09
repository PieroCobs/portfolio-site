<script lang="ts">
	import Project from './project.svelte';
	import Spacer from './spacer.svelte';

	import ayudaMobile from '$lib/images/projects/ayuda-mobile.jpg';
	import ayudaWeb from '$lib/images/projects/ayuda-web.jpg';
	import adeo from '$lib/images/projects/adeo.jpg';
	import spOnboarding from '$lib/images/projects/sp-onboarding.jpg';
	import knoxxiWeb from '$lib/images/projects/knoxxi-web.jpg';
	import knoxxiHealth from '$lib/images/projects/knoxxi-health.jpg';
	import knoxxiDrivv from '$lib/images/projects/knoxxi-drivv.jpg';
	import hempireWeb from '$lib/images/projects/hempire-web.jpg';
	import hempireMobile from '$lib/images/projects/hempire-mobile.jpg';
	import sindor from '$lib/images/projects/sindor.jpg';
	import akSurfside from '$lib/images/projects/ak-surfside.jpg';
	import instantVouchers from '$lib/images/projects/instant-vouchers.jpg';
	import maxitech from '$lib/images/projects/maxitech.jpg';

	type Project = {
		name: string;
		thumb: string;
		roles: string;
		url: string;
	};

	const projects: Project[] = [
		{
			name: 'ayuda mobile',
			thumb: ayudaMobile,
			roles: 'flutter, mobile, UI/UX design',
			url: 'https://ayudahub.com/download'
		},
		{
			name: 'ayuda web',
			thumb: ayudaWeb,
			roles: 'react.js, next.js, UI/UX design',
			url: 'https://ayudahub.com'
		},
		{
			name: 'adeo',
			thumb: adeo,
			roles: 'flutter, mobile, desktop, UI/UX design',
			url: 'https://play.google.com/store/apps/details?id=com.ecoach.adeo'
		},
		{
			name: 'maximal environmental management system',
			thumb: '',
			roles: 'react.js, next.js, UI/UX design',
			url: 'https://mems.maxitechgh.com'
		},
		{
			name: 'ayuda service provider portal',
			thumb: spOnboarding,
			roles: 'react.js, next.js, UI/UX design',
			url: 'https://sp.ayudahub.com'
		},
		{
			name: 'ayuda back office',
			thumb: '',
			roles: 'HTML, SCSS, JavaScript, jQuery, UI/UX design',
			url: 'https://ghana.ayudahub.com'
		},
		{
			name: 'knoxxi web',
			thumb: knoxxiWeb,
			roles: 'react.js, next.js, UI/UX design',
			url: 'https://knoxxi.com'
		},
		{
			name: 'knoxxiHealth',
			thumb: knoxxiHealth,
			roles: 'UI/UX design',
			url: 'https://apps.apple.com/gh/app/knoxxihealth/id1548661611'
		},
		{
			name: 'knoxxiDrivv',
			thumb: knoxxiDrivv,
			roles: 'UI/UX design',
			url: 'https://apps.apple.com/gh/app/knoxxi-drivv/id1570035556'
		},
		{
			name: 'h-empire web',
			thumb: hempireWeb,
			roles: 'react.js, next.js, UI/UX design',
			url: 'https://hempireonline.com'
		},
		{
			name: 'h-empire mobile',
			thumb: hempireMobile,
			roles: 'UI/UX design',
			url: ''
		},
		{
			name: 'sinDor',
			thumb: sindor,
			roles: 'UI/UX design',
			url: ''
		},
		{
			name: 'a&k surfside',
			thumb: akSurfside,
			roles: 'UI/UX design',
			url: ''
		},
		{
			name: 'maxitech gh',
			thumb: maxitech,
			roles: 'react.js, next.js',
			url: 'https://maxitechgh.com'
		},
		{
			name: 'instant vouchers',
			thumb: instantVouchers,
			roles: 'react.js, next.js, UI/UX design',
			url: 'https://instantvouchers.net'
		}
	];
</script>

<div class="projects" id="projects">
	<h2 class="section-title">my latest projects</h2>
	<Spacer height={2} />

	<div class="row">
		{#each projects as project, i}
			<div class="col">
				<Project
					name={project.name}
					thumb={project.thumb}
					roles={project.roles}
					url={project.url}
				/>
			</div>
		{/each}
	</div>
</div>

<style lang="scss">
	.projects {
		margin: $column-margin-top 0;
		border-top: 1px solid $color-border;
		padding-top: $column-margin-top;
	}

	.row {
		margin: 0 -30px;

		.col {
			padding: 40px 30px;
		}

		@media (min-width: 768px) {
			display: flex;
			flex-wrap: wrap;

			.col {
				width: 50%;
			}
		}

		@media (min-width: 1024px) {
			.col {
				width: calc(100% / 3);
			}
		}
	}
</style>
