<script>
	import '../app.css';
</script>

<main class="main">
	<slot />
</main>

<style>
	.main {
		display: grid;
		grid-template-columns: 1fr 2fr;
		padding: 20px;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
		gap: 16px;

		@media (max-width: 1024px) {
			grid-template-columns: 1fr;
			grid-template-rows: auto 1fr;
		}
	}
</style>
