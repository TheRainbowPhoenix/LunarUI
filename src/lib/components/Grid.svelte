<div class="grid">
	<slot />
</div>

<style>
	.grid {
		display: grid;
		grid-template-columns: 1fr 1fr 1fr;
		grid-template-rows: auto;
		gap: 16px;
		place-items: stretch;
		-webkit-box-align: stretch;
		margin-bottom: 16px;
	}
</style>
