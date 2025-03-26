<script>
	import Card from '$components/Card.svelte';
</script>

<section {...$$restProps} class={`experience-section ${$$restProps.class || ''}`}>
	<Card>Experience</Card>
</section>
