<script lang="ts">
	export let discardable = false;
</script>

<div class="card">
	{#if $$slots.header}
		<div class="header">
			<slot name="header" />
		</div>
	{/if}
	{#if $$slots.text}
		<div class="text">
			<slot name="text" />
		</div>
	{/if}
	<slot />
	{#if $$slots.actions}
		<div class="actions">
			<slot name="actions" />
		</div>
	{/if}

	{#if discardable}
		<!-- -->
	{/if}
</div>

<style>
	.card {
		padding: 12px;
		border-radius: 6px;

		display: flex;
		flex: initial;
		flex-direction: column;
		gap: 16px;
	}

	.header {
		display: flex;
		flex: initial;
		flex-direction: row;
		-webkit-box-align: center;
		align-items: center;
		gap: 12px;
	}

	.text {
		color: var(--text-secondary-color);
	}

	.actions {
		display: flex;
		flex: initial;
		flex-direction: row;
		-webkit-box-align: center;
		align-items: center;
	}
</style>
