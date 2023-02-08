<script>
	import Cta from '$lib/components/cta.svelte';
	import EducationExperience from '$lib/components/education-experience.svelte';
	import LandingPage from '$lib/components/landing-page.svelte';
	import Projects from '$lib/components/projects.svelte';
	import Stack from '$lib/components/stack.svelte';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<LandingPage />
<Stack />
<EducationExperience />
<Projects />
<Cta />
