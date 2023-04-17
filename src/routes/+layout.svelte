<script lang="ts">
	import { Button, TextBlock } from "fluent-svelte";
	import '../lib/fonthelper.css';
	import "fluent-svelte/theme.css";
    import Nav from "../layouts/navbar.svelte"
</script>

<div class="app">
    <div class="slot-container">
        <slot />
    </div>
    <Nav />
</div>

<head>
  <title>Rectify11's Website</title>
</head>

<style>
    .slot-container
    {
        background-color: blue;
        overflow-x:hidden;
	    min-height: 100vh;
	    position: absolute;
	    top: 0;
	    left: 0;
	    width: 100vw;
    }
</style>