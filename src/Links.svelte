<script lang="ts">
  const links = [
    {
      url: "siligong.dev",
      name: "Siligong.dev",
    },
    {
      url: "siligong.slack.com",
      name: "Siligong Slack",
    },
    {
      url: "https://www.meetup.com/SiligongValley/",
      name: "Siligong Meetup",
    },
  ];
</script>

<h3>Links</h3>
<ul>
  {#each links as { url, name }, i (url)}
    <li><a target="_blank" href={url}>{i + 1}. {name}</a></li>
  {/each}
</ul>

<style>
  ul {
    text-align: left;
  }
</style>
