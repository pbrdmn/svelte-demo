<script lang="ts">
  import Async from "./Async.svelte";
  import Counter from "./Counter.svelte";
  import Links from "./Links.svelte";
  import Grid from "./components/Grid.svelte";
  import Section from "./components/Section.svelte";

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
  <Grid>
    <Section>
      <Counter on:counterUpdate={onCounterUpdate} />
    </Section>
    <Section>
      <Async />
    </Section>
    <Section>
      <Links />
    </Section>
  </Grid>
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }
</style>
