<script lang="ts">
	export let primary = false;
	export let large = false;
	export let flat = false;
</script>

<button class:flat class:primary class:large type="button">
	<slot />
</button>

<style global>
	button.large {
		min-width: 32px;
		height: 32px;
		padding: 0px 14px;
		font-size: 0.85rem;
	}

	button {
		display: inline-flex;
		-webkit-box-align: center;
		align-items: center;
		-webkit-box-pack: center;
		justify-content: center;
		white-space: nowrap;
		flex-shrink: 0;
		margin: 0px;
		border-radius: 4px;
		font-weight: 500;
		line-height: normal;
		transition-property: border, background-color, color, opacity;
		transition-duration: 0.15s;
		user-select: none;
		position: relative;
		min-width: 24px;
		height: 24px;
		padding: 0px 8px;
		font-size: 0.75rem;
		cursor: pointer;
	}
</style>
