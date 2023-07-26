<script lang="ts">
	import '../global.css';
	import Grid from '$lib/components/Grid.svelte';
	import Card from '$lib/components/Card.svelte';
	import HeaderIcon from '$lib/components/HeaderIcon.svelte';
	import Button from '$lib/components/Button.svelte';
	import Title from '$lib/components/Title.svelte';
	import Separator from '$lib/components/Separator.svelte';
	import SimpleAction from '$lib/composable/SimpleAction.svelte';
	import User from '$lib/components/User.svelte';
	import TextInput from '$lib/components/TextInput.svelte';
</script>

<main id="root">
	<div class="content">
		<Title>Welcome</Title>
		<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

		<Separator />

		<SimpleAction helpLink="#" />

		<Separator />

		<Grid>
			{#each Array.from(Array(5).keys()) as c}
				<Card>
					<HeaderIcon slot="header" text="Title here" />
					<span slot="text">{c} zierhgzei z rhneierkfhuie</span>
					<svelte:fragment slot="actions">
						<Button>Do it now</Button>
					</svelte:fragment>
				</Card>
			{/each}
		</Grid>

		<Separator />

		<User user={{ name: 'test', mail: 'test@localhost' }} />

		<Separator />

		<TextInput name="test" title="Test value" value={'test'} />
		<div style="margin-bottom: 12px;" />
		<TextInput prefix="site/" title="Site slug" value={'dQw4w9WgXcQ'} />

		<Separator />

		<div style="height: 40vh;" />
	</div>
</main>

<style>
	main {
		min-height: 100vh;
	}

	.content {
		max-width: 54rem;
		margin: 0 auto;
		margin-top: 4rem;

		display: flex;
		flex: initial;
		flex-direction: column;
	}
</style>
