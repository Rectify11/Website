<script lang="ts">
    export let hero: string;
    export let name: string;
    export let description: string;

    import { TextBlock } from "fluent-svelte";
</script>

<div class="card">
    <img class="hero" src={hero} alt="feature-hero"/>
    <TextBlock class="name">{name}</TextBlock>
    <TextBlock class="description">{description}</TextBlock>
</div>

<style>
    .card
    {
        backdrop-filter: blur(40px) saturate(100%);
        background-color: rgba(var(--fds-solid-background-base), 0.8);
	    background-blend-mode: darken;
        width: 300px;
        height: 300px;
        border-radius: 8px;
        border: 1px solid rgba(80, 80, 80, 0.226);
        padding: 5px;
        margin: 5px;
        transition: all 0.2s ease-in-out;
    }
    .card:hover
    {
        backdrop-filter: blur(90px) saturate(150%);
    }

    .hero
    {
        height: 60px;
        width: 60px;
        margin-left: -10px;
    }
</style>