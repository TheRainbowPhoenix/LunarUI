<script>
	export let title = 'Title';
	export let value = '';

	export let name = 'name';
	/**
	 * @type string | null
	 */
	export let prefix = null;

	/**
	 * @type HTMLElement | undefined
	 */
	let prefixElem;

	$: padding = prefixElem ? prefixElem.offsetWidth + 10 : 12;
</script>

<div class="input">
	<label for={name}><span>{title}</span></label>
	<div class="field">
		{#if prefix}
			<div class="prefix" bind:this={prefixElem}>
				<span>
					{prefix}
				</span>
			</div>
		{/if}
		<input {name} type="text" autocomplete="off" style="padding-left: {padding}px;" bind:value />
	</div>
</div>

<style>
	.input {
		display: flex;
		flex: initial;
		flex-direction: column;
	}

	label {
		display: block;
		padding-left: 2px;
		margin-bottom: 4px;
	}

	label span {
		font-style: normal;
		line-height: normal;
		text-align: left;
		color: #d4d5e3;
		font-size: 0.8rem;
		font-weight: 500;
	}

	.field {
		display: flex;
		flex: initial;
		flex-direction: row;
		height: 32px;
		max-width: 256px;
		max-height: 32px;
		position: relative;
	}

	.prefix {
		display: flex;
		height: 100%;
		-webkit-box-align: center;
		align-items: center;
		pointer-events: none;

		position: absolute;
		left: 10px;
	}

	.prefix span {
		font-style: normal;
		line-height: normal;
		text-align: left;
		color: var(--text-secondary-color);
		font-size: 0.8rem;
		font-weight: 500;
	}

	input {
		flex: 1 1 0%;
		margin-right: 8px;

		padding: 6px 12px;
		background: #171823;
		border: 1px solid #33354b;
		border-radius: 4px;
		font-size: 0.8125rem;
		color: var(--text-primary-color);
		margin: 0px;
		appearance: none;
		transition: border 0.15s;
	}

	input:not(:disabled):focus,
	input:not(:disabled).focus-visible {
		box-shadow: none;
		border-color: #349fa0;
	}

	input:not(:disabled):hover {
		transition-duration: 0s;
	}
</style>
