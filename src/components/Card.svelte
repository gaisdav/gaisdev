<div {...$$restProps} class={`card ${$$restProps.class || ''}`}>
	<slot />
</div>

<style>
	.card {
		padding: 20px;
		background: var(--bg-content);
		border-radius: 16px;
		border-width: 1px;
		border-style: solid;
		border-color: var(--color-border);
	}
</style>
