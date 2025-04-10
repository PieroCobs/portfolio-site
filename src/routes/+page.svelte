<script>
	import Cta from '$lib/components/cta.svelte';
	import EducationExperience from '$lib/components/education-experience.svelte';
	import LandingPage from '$lib/components/landing-page.svelte';
	import Projects from '$lib/components/projects.svelte';
	import Stack from '$lib/components/stack.svelte';
</script>

<svelte:head>
	<title>Peter Sabla</title>
	<meta
		name="description"
		content="Creative front-end engineer with passion for designing with code. Implements complex interfaces without a loss in aesthetics or functionality."
	/>
</svelte:head>

<LandingPage />
<Stack />
<Projects />
<EducationExperience />
<Cta />
