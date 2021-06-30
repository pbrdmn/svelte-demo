<script lang="ts">
  import { createEventDispatcher } from "svelte";
  const dispatch = createEventDispatcher<{ counterUpdate: number }>();

  let count: number = 0;

  $: dispatch("counterUpdate", count);

  const increment = () => ++count;
  const reset = () => (count = 0);
</script>

<h3>Counter button</h3>
<div>
  <button on:click={increment}>👏 {count}</button>
  <button on:click={reset}>⏪ Reset</button>
</div>
