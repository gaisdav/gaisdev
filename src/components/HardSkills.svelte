<script>
	import Card from '$components/Card.svelte';
</script>

<section {...$$restProps} class={`hard-skills-section ${$$restProps.class || ''}`}>
	<Card>
		<h2 class="about-title">Skills</h2>
		<ul class="skills-list">
			<li>
				Frontend:
				<ul class="included">
					<li>JavaScript (ES20**)</li>
					<li>TypeScript</li>
					<li>React</li>
					<li>NextJS</li>
					<li>Redux</li>
					<li>MobX</li>
					<li>Zustand</li>
					<li>React Native</li>
				</ul>
			</li>
			<li>
				Backend:
				<ul class="included">
					<li>NodeJS</li>
					<li>NestJS</li>
					<li>ExpressJS</li>
					<li>PostgreSQL</li>
					<li>MongoDB</li>
					<li>MySQL</li>
					<li>TypeORM</li>
				</ul>
			</li>
			<li>
				CSS:
				<ul class="included">
					<li>Styled-components</li>
					<li>CSS-in-JS</li>
					<li>PostCSS</li>
					<li>CSS Modules</li>
					<li>Sass</li>
					<li>Tailwind</li>
				</ul>
			</li>
			<li>
				Performance:
				<ul class="included">
					<li>Build tools</li>
					<li>Testing</li>
					<li>Vercel</li>
					<li>CI/CD</li>
					<li>Webpack</li>
					<li>Vite</li>
					<li>Lazy Loading</li>
					<li>Jest</li>
					<li>Storybook</li>
				</ul>
			</li>
		</ul>
	</Card>
</section>

<style>
	.skills-list {
		display: flex;
		gap: 12px;
		flex-direction: column;
		margin-top: 12px;
	}

	.included {
		margin-left: 24px;
		list-style: disc;
	}
</style>
