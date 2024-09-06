<script>
	import Card from '$components/Card.svelte';
</script>

<aside class="aside">
	<Card class="sidebar">
		<h1 class="name">Gaisar Davletkildin</h1>
		<h3 class="position">Senior Frontend Developer</h3>
		<div class="divider"></div>
		<div class="contacts">
			<div class="contact">
				<div>PHONE</div>
				<a class="contact-value" href="tel:+381621147535">+381621147535</a>
				<a class="contact-value" href="tel:+79773495113">+79773495113</a>
			</div>
			<div class="contact">
				<div>EMAIL</div>
				<a class="contact-value" href="mailto:gais.davletkildin@gmail.com"
					>gais.davletkildin@gmail.com</a
				>
			</div>
			<div class="contact">
				<div>GITHUB</div>
				<a class="contact-value" target="_blank" href="https://github.com/gaisdav"
					>https://github.com/gaisdav</a
				>
			</div>
			<div class="contact">
				<div>TELEGRAM</div>
				<a class="contact-value" target="_blank" href="https://t.me/gaisdav">https://t.me/gaisdav</a
				>
			</div>
			<div class="contact">
				<div>LINKEDIN</div>
				<a
					class="contact-value"
					target="_blank"
					href="https://www.linkedin.com/in/gaisdav/?locale=en_US"
					>https://www.linkedin.com/in/gaisdav</a
				>
			</div>
		</div>
	</Card>
</aside>

<style>
	.aside {
		position: sticky;
		top: 0;
		max-width: 300px;

		.name {
			font-size: 24px;
		}

		.divider {
			height: 1px;
			width: 85%;
			background: var(--color-border);
			margin: 8px auto;
		}

		:global(.sidebar) {
			display: flex;
			flex-direction: column;
			gap: 16px;
		}

		.contacts {
			display: flex;
			flex-direction: column;
			gap: 8px;
		}

		.contact-value {
			word-break: break-word;
		}
	}
</style>
