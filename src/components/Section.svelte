<script>
	import Card from '$components/Card.svelte';

	function changeTheme() {
		const html = document.getElementsByTagName('html')[0];
		const isDark = html.getAttribute('data-theme') === 'dark';
		html.setAttribute('data-theme', isDark ? 'light' : 'dark');
	}
</script>

<main class="main">
	<Card class="sidebar">
		<h2 class="about-title">About me</h2>
		<nav class="nav">
			<Card>
				<button on:click={changeTheme}>O</button>
			</Card>
		</nav>

		<div class="divider"></div>

		<p class="text">
			I'm Gaisar, a front-end software engineer with 6 years of experience. My expertise includes
			React, TypeScript, MobX, and NodeJS. Additionally, I have a good knowledge of Vue, React
			Native and Redux.
		</p>
		<p class="text">
			In my testing practices, I rely on industry-standard tools like Jest and Storybook to ensure
			the reliability and quality of my codebase. Throughout my career, I've successfully launched
			numerous projects spanning various technologies, demonstrating my adaptability and versatility
			in delivering high-quality solutions.
		</p>
		<p class="text">
			Currently, I'm immersed in the development of a CRM system tailored specifically for company
			managers. This responsibility has honed my ability to understand complex business needs and
			translate them into robust technical solutions.
		</p>
		<p class="text">
			As an individual, I pride myself on being responsible, open-minded, and honest. I would be
			pleased to offer my skills and experience to your projects. Thank you!
		</p>
	</Card>
</main>

<style>
	.divider {
		height: 4px;
		border-radius: 2px;
		width: 40px;
		background: var(--color-theme-1);
		margin: 10px 0;
	}

	.main {
		position: relative;
		flex: 1;
	}

	.about-title {
		font-size: 32px;
		font-weight: 500;
	}

	.text {
		font-size: 14px;
		margin-bottom: 1rem;

		&:last-child {
			margin-bottom: 0;
		}
	}

	.nav {
		position: absolute;
		right: 0;
		top: 0;

		:global(.card) {
			padding: 14px;
			border-top-left-radius: 0;
			border-bottom-right-radius: 0;
		}
	}

	@media print {
		.nav {
			display: none;
		}
	}
</style>
