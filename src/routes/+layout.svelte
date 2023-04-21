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
</div>
<div class="topNav">
    <Nav/>
</div>

<style>
    .slot-container
    {
        overflow: auto;
        overflow-x: hidden;
	    min-height: 100vh;
	    position: absolute;
	    top: 0;
	    left: 0;
	    width: 100%;
    }

    .topNav
    {
        position: fixed;
        z-index: 10;
        margin: 0;
        margin-top: -8px;
        margin-left: -8px;
    }
</style>