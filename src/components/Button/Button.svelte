<script lang="ts">
	export let rounded: boolean = false;
</script>

<style>
	button, button:active {
		outline: none;
		background: var(--primary-bg);
		border: none;
		color: black;
		border-radius: 4px;

		transition: linear all .1s;
	}

	.rounded, .rounded:active {
		border-radius: 40px;
	}

	button:hover {
		background: var(--secondary-bg);
	}
</style>

<button
	{...$$restProps}
	on:click
	class:rounded
>
	<slot />
</button>
