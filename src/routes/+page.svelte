<script lang="ts">
    import { TextBlock } from "fluent-svelte";
    import Card from "../lib/card/card.svelte";

    const featureCards = [
    {
      name: 'Better scaling',
      description: 'A test card for the feature card UI.',
      hero: "https://upload.wikimedia.org/wikipedia/commons/thumb/8/87/Windows_logo_-_2021.svg/1024px-Windows_logo_-_2021.svg.png"
    },
    {
      name: 'big name',
      description: 'A test card for the feature card UI.',
      hero: "https://upload.wikimedia.org/wikipedia/commons/thumb/8/87/Windows_logo_-_2021.svg/1024px-Windows_logo_-_2021.svg.png"
    },
    {
      name: 'big name',
      description: 'A test card for the feature card UI.',
      hero: "https://upload.wikimedia.org/wikipedia/commons/thumb/8/87/Windows_logo_-_2021.svg/1024px-Windows_logo_-_2021.svg.png"
    },
    {
      name: 'big name',
      description: 'A test card for the feature card UI.',
      hero: "https://upload.wikimedia.org/wikipedia/commons/thumb/8/87/Windows_logo_-_2021.svg/1024px-Windows_logo_-_2021.svg.png"
    },
    {
      name: 'big name',
      description: 'A test card for the feature card UI.',
      hero: "https://upload.wikimedia.org/wikipedia/commons/thumb/8/87/Windows_logo_-_2021.svg/1024px-Windows_logo_-_2021.svg.png"
    },
    {
      name: 'big name',
      description: 'A test card for the feature card UI.',
      hero: "https://upload.wikimedia.org/wikipedia/commons/thumb/8/87/Windows_logo_-_2021.svg/1024px-Windows_logo_-_2021.svg.png"
    },
  ];
</script>
<div id="container">
	<div id="intro">
        <TextBlock variant="display" style="margin-left: 20px; margin-right: 20px; font-size: 60px;">Introducing Rectify11</TextBlock>
        <TextBlock variant="bodyLarge" style="margin-top: 8px; margin-left: 20px; margin-right: 20px;">Improving upon the Windows 11 experience.</TextBlock>
    </div>
    <div id="card-container">
        {#each featureCards as featureCard}
            <Card bind:name={featureCard.name} bind:description={featureCard.description} bind:hero={featureCard.hero}/>
        {/each}
    </div>
</div>

<style>
	#container
    {
        background-color: var(--fds-solid-background-base);
        background-size: cover; 
        width: 100vw;
		min-height: 100vh;
        text-align: center;
        background: url("/src/lib/bloom_dark.jpg") no-repeat center center fixed;
        background-size: cover;
        display: flex;
        flex-direction: column;
        overflow: auto;
        overflow-x: hidden;
        overflow-y: hidden;
    }
    @media (prefers-color-scheme: light) {
        #container 
        {
            background-image: url("/src/lib/bloom_light.jpg");
        }
    }

    #intro
    {
        display: flex;
        flex-direction: column;
        width: auto;
        height: auto;
        margin-top: 100px;
    }

    #card-container
    {
        width: 100vw;
        min-height: 215px;
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        margin-top: 70px;
        vertical-align: middle;
    }
</style>

<head>
  <title>Rectify11 • Home</title>
</head>