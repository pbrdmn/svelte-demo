<script lang="ts">
	let count: number = 0;
    const increment = () => ++count;
    const reset = () => count = 0;
</script>

<div>
    {#if count >= 3}
        🎉🎉🎉
        <button on:click={reset}>👏 {count}</button>
        🎉🎉🎉
    {:else}
        <button on:click={increment}>👏 {count}</button>
    {/if}
</div>