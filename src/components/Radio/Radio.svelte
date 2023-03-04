<script lang="ts">
    import { scale } from 'svelte/transition';

    export let value: any;
    export let checked: any;
</script>

<style>
    div {
        --size: 40px;

        border-radius: 100%;

        width: var(--size);
        height: var(--size);

        border: 1px solid #333333;

        padding: 2px;

        box-sizing: border-box;

        display: flex;
        align-items: center;
        justify-content: center;

        position: relative;
    }

    .checked {
        position: absolute;

        width: 80%;
        height: 80%;

        transition: var(--transition);

        background: var(--primary-bg);

        box-sizing: border-box;
    }

    .checked:hover {
        background: var(--secondary-bg);
    }
</style>

<!-- svelte-ignore a11y-click-events-have-key-events -->
<div on:click={() => checked = value}>
    {#if checked === value}
        <div class="checked" transition:scale />
    {/if}
</div>
