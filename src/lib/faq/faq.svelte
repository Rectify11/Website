<script lang="ts">
    export let question: string;
    export let answer: string;

    import { TextBlock } from "fluent-svelte";
</script>

<div class="card">
    <div class="content">
        <div><img class="hero" src="/images/question.png" alt="question-hero"/></div>
        <div><TextBlock class="question" variant="bodyLarge" style="margin-top: 15px; font-size: 20px;">{question}</TextBlock></div>
    </div>
    <TextBlock class="answer" style="margin-left: 25px; margin-top: auto; margin-right: 20px; margin-bottom:auto;">{answer}</TextBlock>
</div>

<style>
    :root{
        --default-bg: rgba(73, 73, 73, 0.164);
        --hover-bg: rgba(129, 129, 129, 0.164);
    }
    @media (prefers-color-scheme: light) {
        :root
        {
            --default-bg: rgba(173, 172, 172, 0.164);
            --hover-bg: rgba(240, 240, 240, 0.164);
        }
    }
    @media (prefers-color-scheme: dark) {
        :root
        {
            --default-bg: rgba(73, 73, 73, 0.164);
            --hover-bg: rgba(129, 129, 129, 0.164);
        }
    }

    .card
    {
        -webkit-backdrop-filter: blur(40px) saturate(100%);
        backdrop-filter: blur(40px) saturate(100%);
        background-color: var(--default-bg);
	    background-blend-mode: darken;
        width: 350px;
        height: 250px;
        border-radius: 12px;
        border: 1px solid rgba(80, 80, 80, 0.226);
        padding: 0px;
        margin: 5px;
        transition: all 0.2s ease-in-out;
        display: flex;
        flex-direction: column;
        align-items: center;
        overflow: hidden;
    }
    .card:hover
    {
        background-color: var(--hover-bg);
    }

    .hero
    {
        height: 60px;
        width: 60px;
        margin-top: 25px;
    }

    .content {
        display: flex;
        flex-direction: column;
        align-items: center;
    }
</style>