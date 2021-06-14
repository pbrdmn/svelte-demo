<script lang="ts">
	export let count: number = 0;
    export const increment = () => ++count;
</script>

<div>
	<button on:click={increment}>👏 {count}</button>
</div>