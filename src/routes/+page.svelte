<script lang="ts">
    import { TextBlock } from "fluent-svelte";
</script>

<div id="container">
	<div id="intro">
        <TextBlock variant="display" style="margin-left: 20px; margin-right: 20px;">Introducing Rectify11</TextBlock>
    </div>
</div>

<style>
	#container
    {
        background-color: var(--fds-solid-background-base);
        background-size: cover;
        width: 100vw;
		height: 100vh;
		overflow-x: hidden;
        text-align: center;
        background-image: url("/src/lib/bloom_dark.jpg");
        background-size: cover;
        background-position: center;
    }
    @media (prefers-color-scheme: light) {
        #container 
        {
            background-image: url("/src/lib/bloom_light.jpg");
        }
    }

    #intro
    {
        display: inline-block;
        width: auto;
        height: auto;
        margin: 0 auto;
        margin-top: 80px;
    }
</style>

<head>
    <title>Rectify11 • Home</title>
</head>