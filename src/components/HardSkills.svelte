<script>
	import Card from '$components/Card.svelte';
</script>

<section {...$$restProps} class={`hard-skills-section ${$$restProps.class || ''}`}>
	<Card>
		<h2 class="about-title">Skills</h2>
		<div>
			React Vue TypeScript JavaScript ReactNative MobX Redux Webpack CSS Modules Styled-components
			Postgres NodeJS NestJS MongoDB MySQL Jest TypeORM
		</div>
	</Card>
</section>

<style>
</style>
