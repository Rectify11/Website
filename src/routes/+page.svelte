<script lang="ts">
    import { TextBlock } from "fluent-svelte";
    import Card from "../lib/card/card.svelte";

    const featureCards = [
    {
      name: 'Better scaling',
      description: 'Rectify11 makes UI controls consistent on different resolutions and scaling levels.',
      hero: "https://github.com/MishaProductions/Rectify11Installer/blob/master/Rectify11Installer/Resources/scaling.png?raw=true"
    },
    {
      name: 'Better UI',
      description: 'We have replaced most legacy icons with modern icons and updated older MetroUI based dialogs.',
      hero: "https://github.com/MishaProductions/Rectify11Installer/blob/master/Rectify11Installer/Resources/menusD.png?raw=true"
    },
    {
      name: 'Rectify11 has a more consistent theme',
      description: 'We have tried our best to replicate WinUI controls in our themes and adds proper dark theme support to most apps.',
      hero: "https://github.com/MishaProductions/Rectify11Installer/blob/master/Rectify11Installer/Resources/ui.png?raw=true"
    },
    {
      name: 'Rectify11 has better performance',
      description: 'In future releases, you will be able to choose things that you want to debloat in your system.',
      hero: "https://github.com/MishaProductions/Rectify11Installer/blob/master/Rectify11Installer/Resources/performance.png?raw=true"
    },
    {
      name: 'Better experience',
      description: 'Rectify11 adds many quality of life fixes to Windows 11, such as resizing the checkboxes as you change the view in File Explorer',
      hero: "https://github.com/MishaProductions/Rectify11Installer/blob/master/Rectify11Installer/Resources/cool.png?raw=true"
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
        min-height: 225px;
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