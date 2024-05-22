<script lang="ts">
	import { Button, TextBlock, IconButton } from "fluent-svelte";
	import '../lib/fonthelper.css';
	import "fluent-svelte/theme.css";
	import * as links from "../lib/links";

	function toggleNavMenu() {
    	openNavMobile = !openNavMobile;
  	}
	let openNavMobile = false;
</script>

<div class="mobileNavMenu" class:showMobileNav={openNavMobile}>
	<div class="mobileNavButton">
		<Button variant="hyperlink" height="20px" href="/" on:click={toggleNavMenu}>
			<TextBlock>Home</TextBlock>
		</Button>
	</div>
	<div class="mobileNavButton">
		<Button variant="hyperlink" height="20px" href="{links.discordLink}" on:click={toggleNavMenu}>
			<TextBlock>Discord Server</TextBlock>
		</Button>
	</div>
	<div class="mobileNavButton">
		<Button variant="hyperlink" height="20px" href="/faq" on:click={toggleNavMenu}>
			<TextBlock>FAQ</TextBlock>
		</Button>
	</div>
	<div class="mobileNavButton">
		<Button variant="hyperlink" height="20px" href="{links.gitHubSrcLink}" on:click={toggleNavMenu}>
			<TextBlock>GitHub</TextBlock>
		</Button>
	</div>
	<div class="mobileNavButton">
		<Button variant="accent" height="20px" style="cursor: pointer;" href="{links.gitHubLink}">
			<TextBlock style="font-family: SegoeFlnt; height: 10px; margin-top: 0px; margin-right: 4px; margin-top: -8px; margin-left: -2px; padding: 0px;">&#xE118;</TextBlock>  Download
		</Button>
	</div>
</div>

<div id="topNavbar">
	<a href="/"><img id="r11Icon" src="/rectify11_logo.png" alt="Rectify11 Logo" height="35"/></a>
	<div class="r11Banner"><TextBlock variant="bodyLarge" style="font-size:25px; margin-top: 17px; margin-left: 8px;">Rectify11</TextBlock></div>
	<div id="rightMobileControl">
		<IconButton on:click={toggleNavMenu}>
			<svg width="16" height="11" viewBox="0 0 16 11" fill="none" xmlns="http://www.w3.org/2000/svg">
				<path d="M0.5 1C0.364583 1 0.247396 0.950521 0.148438 0.851562C0.0494792 0.752604 0 0.635417 0 0.5C0 0.364583 0.0494792 0.247396 0.148438 0.148438C0.247396 0.0494792 0.364583 0 0.5 0H15.5C15.6354 0 15.7526 0.0494792 15.8516 0.148438C15.9505 0.247396 16 0.364583 16 0.5C16 0.635417 15.9505 0.752604 15.8516 0.851562C15.7526 0.950521 15.6354 1 15.5 1H0.5ZM0.5 6C0.364583 6 0.247396 5.95052 0.148438 5.85156C0.0494792 5.7526 0 5.63542 0 5.5C0 5.36458 0.0494792 5.2474 0.148438 5.14844C0.247396 5.04948 0.364583 5 0.5 5H15.5C15.6354 5 15.7526 5.04948 15.8516 5.14844C15.9505 5.2474 16 5.36458 16 5.5C16 5.63542 15.9505 5.7526 15.8516 5.85156C15.7526 5.95052 15.6354 6 15.5 6H0.5ZM0.5 11C0.364583 11 0.247396 10.9505 0.148438 10.8516C0.0494792 10.7526 0 10.6354 0 10.5C0 10.3646 0.0494792 10.2474 0.148438 10.1484C0.247396 10.0495 0.364583 10 0.5 10H15.5C15.6354 10 15.7526 10.0495 15.8516 10.1484C15.9505 10.2474 16 10.3646 16 10.5C16 10.6354 15.9505 10.7526 15.8516 10.8516C15.7526 10.9505 15.6354 11 15.5 11H0.5Z" fill="white"/>
			</svg>			
		</IconButton>
	</div>
	<div id="rightControls">
		<Button variant="hyperlink" height="20px" style="margin-right: 10px;" href="{links.discordLink}">
			<TextBlock>Discord Community</TextBlock>
		</Button>
		<Button variant="hyperlink" height="20px" style="margin-right: 20px;" href="/faq">
			<TextBlock>FAQ</TextBlock>
		</Button>
		<Button variant="hyperlink" height="20px" style="margin-right: 20px;" href="{links.gitHubSrcLink}">
			<TextBlock>GitHub</TextBlock>
		</Button>
		<Button variant="accent" height="20px" style="cursor: pointer;" href="{links.gitHubLink}">
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
	  backdrop-filter: blur(10px) saturate(100%);
	  -webkit-backdrop-filter: blur(20px) saturate(100%);
	  background-blend-mode: darken;
	  position: absolute;
	  display: flex;
  }
  
  .mobileNavMenu
  {
	background-color: #343333ba;
	width: 210px;
	height: 100vh;
	backdrop-filter: blur(20px) saturate(100%);
	-webkit-backdrop-filter: blur(20px) saturate(100%);
	position: fixed;
	right: -210px;
	margin-top: 60px;
	transition: all 0.2s ease-in-out;
	background-blend-mode: darken;
  }

  @media (prefers-color-scheme: light) {
        #topNavbar
        {
            background-color: #f5f5f594;
			background-blend-mode: normal;
        }
		.mobileNavMenu {
        	background-color: #f5f5f594;
			background-blend-mode: normal;
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

		.r11Banner
		{
			visibility: collapse;
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
		
		.r11Banner
		{
			visibility: visible;
		}
  }
  
  #rightControls
  {
	  margin-top: 15px;
	  display: flex;
	  align-items: center;
	  position: absolute;
	  right: 0;
	  margin-right: 20px;
  }

  .showMobileNav
  {
	right: 0;
  }

  #rightMobileControl
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

  .mobileNavButton
  {
	width: 205px;
	display: flex;
	justify-content: center;
	margin-top: 20px;
  }

</style>
