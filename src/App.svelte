<script lang="ts">
  import Async from "./Async.svelte";
  import Counter from "./Counter.svelte";
  import Links from "./Links.svelte";
  export let name: string;

  const onCounterUpdate = ({ detail }: CustomEvent<number>) =>
    console.log("counter update:", detail);
</script>

<main>
  <h1>Hello {name}!</h1>
  <p>
    Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn
    how to build Svelte apps.
  </p>
  <Counter on:counterUpdate={onCounterUpdate} />
  <Async />
  <Links />
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
