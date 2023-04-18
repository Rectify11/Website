<script lang="ts">
    import { TextBlock } from "fluent-svelte";
</script>

<div id="container">
	<div id="intro">
        <TextBlock variant="display" style="margin-left: 10px; margin-right: 10px;">Introducing Rectify11</TextBlock>
    </div>
</div>

<style>
	#container
    {
        background-color: var(--fds-solid-background-base);
        background-image: url("./static/images/bloom_light.jpg");
        background-size: cover;
        width: 100vw;
		height: 100vh;
		overflow-x: hidden;
        text-align: center;
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