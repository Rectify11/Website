<script lang="ts">
	import { Button, TextBlock } from "fluent-svelte";
	import '../lib/fonthelper.css';
	import "fluent-svelte/theme.css";
</script>
  
  <div id="topNavbar">
	<a href="/"><img id="r11Icon" src="/rectify11_logo.png" alt="Rectify11 Logo" height="35"/></a>
	  <div id="rightControls">
		  <Button variant="hyperlink" height="20px" style="margin-right: 10px;" href="/community">
			  <TextBlock style="color:#B0B2B7;">Community</TextBlock>
		  </Button>
		  <Button variant="hyperlink" height="20px" style="margin-right: 20px;" href="/faq">
			  <TextBlock style="color:#B0B2B7;">FAQ</TextBlock>
		  </Button>
		  <Button variant="accent" height="20px" style="cursor: pointer;" href="/download">
			  <TextBlock style="font-family: SegoeFlnt; height: 10px; margin-top: 0px; margin-right: 4px; margin-top: -8px; margin-left: -2px; padding: 0px;">&#xE118;</TextBlock>  Download
		  </Button>
	  </div>
  </div>
  
  <style>
	  :global(body) {
		  /*background: url("https://4kwallpapers.com/images/wallpapers/windows-11-dark-background-bloom-5k-5120x2880-8399.png");*/
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
	  display: flex;
  }
  
  #rightControls
  {
	  margin-left: auto;
	  margin-right: 20px;
  
	  display: flex;
		align-items: center;
  }
  
  #r11Icon
  {
	  margin-top: 12px;
	  margin-left: 12px;
	  cursor: pointer;
  }

  </style>

<head>
  <title>Rectify11's Website - Home</title>
</head>
  