<script lang="ts">
    import Faq from "$lib/faq/faq.svelte";
    import { TextBlock } from "fluent-svelte";
    import { InfoBar } from "fluent-svelte";
    export const prerender = true;

    const faqCards = [
        {
            question: 'What are the minimum system requirements to run Rectify11?',
            answer: 'A Windows 11 PC with at least 1GB free space. Supported devices are recommended, but not required.',
        },
        {
            question: 'Where is the ISO?',
            answer: 'We have removed all ISOs as they have been replaced with our installer. ISO patching will be added to the installer in V4.',
        },
        {
            question: 'How do I uninstall Rectify11?',
            answer: 'You can use the "Uninstall" button in the Rectify11 Installer on versions RC1 and up.',
        },
        {
            question: 'Is Rectify11 free?',
            answer: 'Yes - Rectify11 is made for the community, by the community. We maintain the source code under the GNU General Public License.'
        }
    ];
</script>
<div id="container">
      <!--Todo: fix container spacing-->
  <br><br><br><br>
  <InfoBar
    title="Maintenance warning"
    message="This website will be unavailable in preparation for the V4 update from July 1st 2024 to July 10th (time may vary). Thank you!"
    severity="caution"
    closable={false}/>
	<div id="intro">
        <TextBlock variant="display" style="margin-left: 20px; margin-right: 20px; font-size: 60px;">Rectify11 FAQ</TextBlock>
    </div>
    <div id="card-container">
        {#each faqCards as faqCard}
            <Faq bind:question={faqCard.question} bind:answer={faqCard.answer}/>
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
        background: url("/src/lib/dark_bg.png") no-repeat center center fixed;
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
            background-image: url("/src/lib/light_bg.png");
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
        cursor: pointer;
    }
</style>

<svelte:head>
    <title>Rectify11 • FAQ</title>
</svelte:head>
