<script>
	export let children;
</script>

<div class="container">
	<slot />
</div>

<style>
	.container {
		display: grid;
		grid-template-columns: 1fr 1fr;
		grid-template-rows: 1fr 1fr;
		justify-content: center;
		align-items: center;
	}
</style>
