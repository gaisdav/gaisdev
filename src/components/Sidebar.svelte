<script>
	import Card from '$components/Card.svelte';
	import Contacts from '$components/Contacts.svelte';
	import avatar from '$lib/images/avatar.png';
</script>

<aside class="aside">
	<Card class="sidebar">
		<div class="main-info">
			<img class="avatar" src={avatar} alt="Gaisar Davletkildin. Avatar. CV. Resume." />
			<div class="name-wrapper">
				<h1 class="name">Gaisar Davletkildin</h1>
				<h3 class="position">Senior Frontend Developer</h3>
			</div>
		</div>
		<div class="divider"></div>
		<Contacts />
	</Card>
</aside>

<style>
	.aside {
		.avatar {
			width: 60%;
			border-radius: 25%;
			margin: 0 auto;
		}

		.name {
			text-align: center;
			font-size: 24px;
		}

		.position {
			text-align: center;
		}

		.divider {
			height: 1px;
			width: 85%;
			background: var(--color-border);
			margin: 8px auto;
		}

		.main-info {
			display: grid;
			gap: 16px;
		}

		.name-wrapper {
			display: flex;
			flex-direction: column;
			justify-content: flex-start;
			gap: 8px;
		}

		:global(.sidebar) {
			display: flex;
			flex-direction: column;
			gap: 16px;
		}

		@media (max-width: 1024px) {
			.divider {
				width: 100%;
			}

			.main-info {
				display: grid;
				grid-template-columns: auto 1fr;
				justify-content: center;
			}

			.avatar {
				width: 120px;
			}

			.name-wrapper {
				justify-content: center;
			}

			.name,
			.position {
				text-align: left;
				line-height: 1.1;
			}
		}

		@media (max-width: 768px) {
			.name {
				font-size: 20px;
			}

			.position {
				font-size: 16px;
			}

			.avatar {
				width: 80px;
			}
		}
	}
</style>
