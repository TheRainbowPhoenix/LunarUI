<script>
	import Button from '$lib/components/Button.svelte';

	export let action = true;
	/**
	 * @type string | null
	 */
	export let helpLink = null;
</script>

<div class="actionnable">
	<div>
		<span class="name"><slot name="name">Name</slot></span>
		<div class="description">
			TODO here zsifzeofjzcb ozefihf jozfde
			{#if helpLink}
				<a href={helpLink} class="helpLink">Read more</a>
			{/if}
		</div>
	</div>
	{#if action}
		<Button primary={true} large={true}>Action</Button>
	{/if}

	<slot />
</div>

<style>
	.actionnable {
		display: flex;
		flex: initial;
		flex-direction: row;
		-webkit-box-pack: justify;
		justify-content: space-between;
	}

	.name {
		font-style: normal;
		line-height: normal;
		text-align: left;
		color: var(--text-primary-color);
		font-size: 0.8rem;
		font-weight: 500;

		display: block;
		margin-bottom: 5px;
	}

	.helpLink {
		color: var(--text-primary-color);
	}

	.helpLink::after {
		margin-left: 4px;
		content: '→';
	}

	.description {
		color: var(--text-secondary-color);
		font-size: 0.8rem;
		margin-bottom: 20px;
		margin-right: 16px;
	}
</style>
