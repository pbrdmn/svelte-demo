<script>
    const links = [
        {
            'url': 'siligong.dev',
            'name': 'Siligong.dev'
        },{
            'url': 'siligong.slack.com',
            'name': 'Siligong Slack'
        },{
            'url': 'https://www.meetup.com/SiligongValley/',
            'name': 'Siligong Meetup'
        }
    ];
</script>

<ul>
    {#each links as { url, name }, i}
        <li><a target="_blank" href={url}>{i + 1}. {name}</a></li>
    {/each}
</ul>

<style>
    ul {
        text-align: left;
    }
</style>