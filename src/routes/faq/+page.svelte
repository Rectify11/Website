<script lang="ts">
    import { TextBlock } from "fluent-svelte";
    export const prerender = true;
</script>
<div id="container">
	<div id="intro">
        <TextBlock variant="display" style="margin-left: 20px; margin-right: 20px; font-size: 60px;">FAQ</TextBlock>
        <TextBlock variant="subtitle" style="margin-top: 8px; margin-left: 20px; margin-right: 20px;">What are the system requirements to run Rectify11?</TextBlock>
        <TextBlock variant="subtitle" style="margin-top: 8px; margin-left: 20px; margin-right: 20px; font-size:15px;">A Windows 11 PC with at least 1GB free space.</TextBlock>
        <TextBlock variant="subtitle" style="margin-top: 8px; margin-left: 20px; margin-right: 20px;font-style:bold;">Where is the ISO?</TextBlock>
        <TextBlock variant="subtitle" style="margin-top: 8px; margin-left: 20px; margin-right: 20px;font-size:15px;">Starting with V3, we have removed all ISOs and it replaced it with our installer. ISO patching will be added to the installer in V4.</TextBlock>
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
</style>

<head>
  <title>Rectify11 • Home</title>
</head>