<script lang="ts">
	export let user = { name: 'test', mail: 'test@localhost' };

	let colorHue = 36;
</script>

<div class="flex user">
	<div class="text-ellipsis details">
		<a href="#" draggable="false" tabindex="-1">
			<div class="avatar" aria-label="Avatar image" style="--color-hue: {colorHue};">O3</div>
			<span class="status status-offline" />
		</a>
		<div class="text-ellipsis infos">
			<span class="username">{user.name}</span>
			<span class="mail">{user.mail}</span>
		</div>
	</div>
	<div class="roles">
		<span>Admin</span>
	</div>
	<div class="actions">...<!-- TODO: menu--></div>
</div>

<style>
	.user {
		display: grid;
		column-gap: 16px;
		grid-template-columns: 7fr 3fr 2fr;
		height: 60px;
		min-width: 0px;
	}

	.flex {
		/* display: flex; */
		flex: 1 1 auto;
		flex-direction: row;
		-webkit-box-align: center;
		align-items: center;
		gap: 16px;
	}

	.text-ellipsis {
		white-space: nowrap;
		overflow: hidden;
		text-overflow: ellipsis;
	}

	.details {
		display: flex;
		flex: initial;
		flex-direction: row;
		-webkit-box-align: center;
		align-items: center;
		gap: 16px;
	}

	.details a {
		display: inline-block;
		position: relative;
		line-height: 0;
		flex-shrink: 0;
		aspect-ratio: 1 / 1;
		width: 24px;
		height: 24px;
		font-size: 11px;
	}

	.avatar {
		display: flex;
		border-radius: 50%;
		width: 100%;
		height: 100%;
		color: #fff;
		background-color: hsl(var(--color-hue), 78%, 40%);
		-webkit-box-align: center;
		align-items: center;
		-webkit-box-pack: center;
		justify-content: center;
		flex-shrink: 0;
	}

	.status {
		position: absolute;
		width: 8px;
		height: 8px;
		bottom: -1px;
		right: -1px;

		border-radius: 50%;
	}

	.infos {
		display: flex;
		flex: initial;
		flex-direction: column;
		gap: 4px;
	}

	.username {
		font-style: normal;
		line-height: normal;
		text-align: left;
		white-space: nowrap;
		overflow: hidden;
		text-overflow: ellipsis;
		color: var(--text-primary-color);
		font-size: 0.8rem;
		font-weight: 500;
	}

	.mail {
		font-style: normal;
		line-height: normal;
		font-weight: normal;
		text-align: left;
		white-space: nowrap;
		overflow: hidden;
		text-overflow: ellipsis;
		color: var(--text-secondary-color);
		font-size: 0.8rem;
		user-select: text;
	}

	.roles {
		display: flex;
		flex-shrink: initial;
		flex-basis: initial;
		flex-direction: row;
		-webkit-box-flex: 1;
		flex-grow: 1;
		gap: 8px;
		color: var(--text-primary-color);
	}

	.actions {
		display: flex;
		flex: initial;
		flex-direction: row;
		-webkit-box-align: center;
		align-items: center;
		-webkit-box-pack: end;
		color: var(--text-primary-color);
		justify-content: flex-end;
	}
</style>
