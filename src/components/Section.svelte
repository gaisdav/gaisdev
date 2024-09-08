<script lang="ts">
	import Card from '$components/Card.svelte';
	import LightModeIcon from '$components/LightModeIcon.svelte';
	import DarkModeIcon from '$components/DarkModeIcon.svelte';
	import { onMount } from 'svelte';

	let mode: string | null = null;

	onMount(() => {
		const savedTheme = localStorage.getItem('theme');
		mode = savedTheme || 'dark';

		applyTheme(mode);
	});

	function applyTheme(mode: string) {
		document.documentElement.setAttribute('data-theme', mode);
		localStorage.setItem('theme', mode);
	}

	function changeTheme() {
		mode = mode === 'dark' ? 'light' : 'dark';
		applyTheme(mode);
	}
</script>

<main class="main">
	<Card class="sidebar">
		<h2 class="about-title">About me</h2>
		{#if mode}
			<nav class="nav">
				<Card>
					<button class="theme-switcher" onclick={changeTheme} aria-label="theme-switcher">
						{#if mode === 'dark'}
							<LightModeIcon class="icon" />
						{:else}
							<DarkModeIcon class="icon" />
						{/if}
					</button>
				</Card>
			</nav>
		{/if}

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

		.theme-switcher {
			background: none;
			border: none;
			cursor: pointer;
			padding: 0;
			margin: 0;
			height: 24px;

			:global(.icon) {
				animation: scale-in 0.3s ease;
			}
		}
	}

	@media print {
		.nav {
			display: none;
		}
	}

	[data-theme='light']:root {
		.theme-switcher {
			:global(.icon) {
				fill: var(--color-text);
			}
		}
	}

	@keyframes scale-in {
		from {
			opacity: 0;
			transform: scale(0.5);
		}
		to {
			opacity: 1;
			transform: scale(1);
		}
	}
</style>
