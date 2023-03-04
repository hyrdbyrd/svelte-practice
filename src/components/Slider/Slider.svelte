<style>
	nav {
		display: flex;
		align-items: center;
		justify-content: space-between;
	}

	.container {
		width: 100%;
		max-width: 100vw;
		overflow-x: hiddne;
	}

	.list {
		transition: all linear .2s;

		min-width: 100%;

		display: flex;
		flex-wrap: nowrap;
	}

	:global(.list > *) {
		min-width: 100%;
		max-height: 30vh;
		object-fit: contain;
	}
</style>

<script lang="ts">
	import Button from '../Button/Button.svelte';
    import RadioGroup from '../RadioGroup/RadioGroup.svelte';

	export let checked: number = 0;

	let list: HTMLDivElement;

	$: items = [...(list ? list.children : [])];

	$: {
		if (checked >= items.length) checked = 0;
		else if (checked < 0) checked = items.length - 1;
	}

	const stepTo = (diff = 1) => () => checked += diff;

	const next = stepTo(1);
	const prev = stepTo(-1);
</script>

<div class="container">
	<div bind:this={list} class="list" style:transform="translate(-{checked * 100}%)">
		<slot />
	</div>
</div>

<nav>
	<Button on:click={prev}>Left</Button>
	<RadioGroup values={[...items.keys()]} bind:checked />
	<Button on:click={next}>Right</Button>
</nav>
