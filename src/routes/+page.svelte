<script>
	import Sidebar from '$components/Sidebar.svelte';
	import Section from '$components/Section.svelte';

	const title = 'Gaisar Davletkildin. CV.';
</script>

<svelte:head>
	<title>{title}</title>
	<meta name="description" content={title} />
</svelte:head>

<Sidebar />
<Section />
