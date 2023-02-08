<script>
	import Social from './social.svelte';

	let today = new Date();
</script>

<footer class="footer">
	<div class="copyright">&copy; {today.getFullYear()}. All rights reserved</div>
	<!-- <div class="email">rickpiero237@gmail.com</div> -->
	<Social />
</footer>

<style lang="scss">
	.footer {
		margin: $column-margin-top 0;
		border-top: 1px solid $color-border;
		padding-top: $column-margin-top;
		display: flex;
		justify-content: space-between;
		align-items: center;
		text-transform: uppercase;
		font-size: 12px;
		font-weight: 600;

		@media (min-width: 769px) {
			margin-top: calc($column-margin-top * 2);
		}
	}
</style>
