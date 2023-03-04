<style>
    div {
        display: flex;
        align-items: center;
        justify-content: space-around;
        width: 100%;
    }
</style>

<script lang="ts">
    import Radio from "../Radio/Radio.svelte";

    type T = $$Generic;

    export let values: T[] = [];
    export let checked: T = values[0];
</script>

<div>
    {#each values as value}
        <Radio {value} bind:checked />
    {/each}
</div>
