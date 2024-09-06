<script>
	import '../app.css';
</script>

<main class="main">
	<slot />
</main>

<style>
	.main {
		flex: 1;
		display: flex;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
		gap: 16px;
	}
</style>
