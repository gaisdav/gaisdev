<script>
	import MainInfo from '$components/MainInfo.svelte';
	import Section from '$components/Section.svelte';
	import HardSkills from '$components/HardSkills.svelte';

	const title = 'Gaisar Davletkildin. CV.';
</script>

<svelte:head>
	<title>{title}</title>
	<meta name="description" content={title} />
</svelte:head>

<main class="main">
	<MainInfo />
	<HardSkills />
	<Section />
</main>

<style>
	:global(.main-info-section) {
		grid-area: main-info;
	}
	:global(.hard-skills-section) {
		grid-area: hard-skills;
	}
	:global(.about) {
		grid-area: about;
	}

	.main {
		display: grid;
		grid-template-columns: 1fr 2fr;
		padding: 20px;
		width: 100%;
		height: min-content;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
		gap: 16px;
		grid-template-areas:
			'main-info   about'
			'hard-skills about';

		@media (max-width: 1024px) {
			grid-template-columns: 1fr;
			grid-template-areas:
				'main-info'
				'about'
				'hard-skills';
		}
	}
</style>
