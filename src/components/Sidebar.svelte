<script>
	import CV from '$lib/pdfs/Gaisar Davletkildin (CV Frontend).pdf';
	import Card from '$components/Card.svelte';
</script>

<aside class="aside">
	<Card class="sidebar">
		<h1 class="name">Gaisar Davletkildin</h1>
		<a href={CV} download>Download CV</a>
	</Card>
</aside>

<style>
	.aside {
		position: sticky;
		top: 0;

		.name {
			font-size: 24px;
		}

		:global(.sidebar) {
			display: flex;
			flex-direction: column;
			gap: 16px;
		}
	}
</style>
