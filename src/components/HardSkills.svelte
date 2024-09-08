<script>
	import Card from '$components/Card.svelte';
</script>

<section {...$$restProps} class={`hard-skills-section ${$$restProps.class || ''}`}>
	<Card>
		<h2 class="about-title">Skills</h2>
	</Card>
</section>

<style>
</style>
