<script>
	import CV from '$lib/pdfs/Gaisar Davletkildin (CV Frontend).pdf';

	const title = 'My CV!';
</script>

<svelte:head>
	<title>{title}</title>
	<meta name="description" content={title} />
</svelte:head>

<section>
	<h1>{title}</h1>

	<h2>Hi! Here is my CV.</h2>
	<div>
		<div>
			<a href={CV} download>download CV</a>
		</div>
		<div>
			<a href={CV} target="_blank">open in the new tab</a>
		</div>
	</div>
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
	}
</style>
