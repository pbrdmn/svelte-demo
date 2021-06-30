<script lang="ts">
  let timer;
  let done: boolean = true;
  const startTimer = () => {
    done = false;
    timer = setTimeout(() => (done = true), 1000);
  };
</script>

<h3>Async button</h3>
<button on:click={startTimer} aria-disabled={!done}
  >{done ? "🛑 Done" : "⏳ Wait"}</button
>

<style>
  button[aria-disabled="true"] {
    opacity: 0.5;
    pointer-events: none;
  }
</style>
