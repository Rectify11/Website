<script lang="ts">
	import { Button, TextBlock, IconButton } from "fluent-svelte";
	import '../lib/fonthelper.css';
	import "fluent-svelte/theme.css";
</script>
  
<div id="topNavbar">
	<a href="/"><img id="r11Icon" src="/rectify11_logo.png" alt="Rectify11 Logo" height="35"/></a>
	<div id="rightMobileControl">
		<IconButton>
			
		</IconButton>
	</div>
	<div id="rightControls">
		<Button variant="hyperlink" height="20px" style="margin-right: 10px;" href="/community">
			<TextBlock>Community</TextBlock>
		</Button>
		<Button variant="hyperlink" height="20px" style="margin-right: 20px;" href="/faq">
			<TextBlock>FAQ</TextBlock>
		</Button>
		<Button variant="accent" height="20px" style="cursor: pointer;" href="/download">
			<TextBlock style="font-family: SegoeFlnt; height: 10px; margin-top: 0px; margin-right: 4px; margin-top: -8px; margin-left: -2px; padding: 0px;">&#xE118;</TextBlock>  Download
		</Button>
	</div>
</div>
  
  <style>
	  :global(body) {
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
	  background-blend-mode: darken;
	  position: absolute;
	  display: flex;
  }
  @media (prefers-color-scheme: light) {
        #topNavbar
        {
            background-color: #a6a4a4ba;
			background-blend-mode: darken;
        }
  }
  @media (max-width: 768px) {
		#rightControls
		{
			visibility: collapse;
		}
		#rightMobileControl
		{
			visibility: visible;
		}
  }
  @media (min-width: 769px) {
		#rightControls
		{
			visibility: visible;
		}
		#rightMobileControl
		{
			visibility: collapse;
		}
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
  