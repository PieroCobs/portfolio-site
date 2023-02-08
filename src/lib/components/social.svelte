<script>
	import FaLinkedinIn from 'svelte-icons/fa/FaLinkedinIn.svelte';
	import IoIosCall from 'svelte-icons/io/IoIosCall.svelte';
	import IoLogoGithub from 'svelte-icons/io/IoLogoGithub.svelte';
	import MdMailOutline from 'svelte-icons/md/MdMailOutline.svelte';
</script>

<div class="social">
	<div class="icon">
		<a href="tel:+233247081117"><IoIosCall /></a>
	</div>
	<div class="icon">
		<a href="mailto:rickpiero237@gmail.com"><MdMailOutline /></a>
	</div>
	<div class="icon">
		<a href="https://gh.linkedin.com/in/peter-sabla-963b64116" target="_blank" rel="noreferrer"
			><FaLinkedinIn /></a
		>
	</div>
	<div class="icon">
		<a href="https://github.com/pierocobs" target="_blank" rel="noreferrer"><IoLogoGithub /></a>
	</div>
</div>

<style lang="scss">
	.social {
		display: flex;
		align-items: center;
	}

	.icon {
		width: 16px;

		&:not(:last-child) {
			margin-right: 20px;
		}
	}
</style>
