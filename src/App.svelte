<script lang="ts">
  import { Button } from "fluent-svelte";
  import './lib/fonthelper.css';
  import "fluent-svelte/theme.css";
</script>

<div id="topNavbar">
    <img id="r11Icon" src="/rectify11_logo.png" alt="Rectify11 Logo" height="35"/>
	<Button variant="accent" height="20px">
		<p style="font-family: SegoeFlnt; height: 10px; margin-top: 0px; margin-right: 4px; margin-top: 2px; padding: 0px;">&#xE118;</p>  Download
	</Button>
</div>

<style>
	:global(body) {
		background: url("https://4kwallpapers.com/images/wallpapers/windows-11-dark-background-bloom-5k-5120x2880-8399.png");
		background-position: absolute;
		background-size: cover;
		background-color: var(--fds-solid-background-base);
		color: var(--fds-text-primary);
		color-scheme: dark;
	}
	@media (prefers-color-scheme: light) {
	:global(body) {
		background-color: white;
		color-scheme: light;
	}
}

#topNavbar
{
    background-color: #343333ba;
    overflow-x:hidden;
    overflow-y: hidden;
    height: 60px;
    position: absolute;
    top: 0;
	left: 0;
    width: 100vw;
    backdrop-filter: blur(40px) saturate(400%);
    background-blend-mode: lighten;
	position: absolute;
}

#r11Icon
{
	margin-top: 12px;
	margin-left: 12px;
}
</style>

