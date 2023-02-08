<script>
	import AnchorButton from './anchor-button.svelte';
	import Spacer from './spacer.svelte';
</script>

<div class="cta" id="contact">
	<h2 class="section-title">what are you working on?</h2>
	<Spacer height={1} />
	<p>
		Let's have a conversation. I'd love to hear about what you're working on and find a way to work
		together.
	</p>
	<Spacer height={2} />
	<AnchorButton href="mailto:rickpiero237@gmail.com" label="Get in touch" />
</div>

<style lang="scss">
	.cta {
		margin: $column-margin-top 0;
		border-top: 1px solid $color-border;
		padding-top: $column-margin-top;
		text-align: center;
	}

	p {
		width: 100%;
		max-width: 400px;
		margin: 0 auto;
	}
</style>
