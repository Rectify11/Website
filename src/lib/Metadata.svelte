<script lang="ts">
	export let title = "Rectify11";
	export let heroImage = "";
	export let description = "Official Rectify11 Website";
	export let imageHost = "";
	export let imageProtocol = "";
</script>

<svelte:head>
	<title>{title}</title>
	<meta content={title} name="og:title" />
	{#if heroImage && imageHost && imageProtocol}
		<meta
			content="{imageProtocol}//{imageHost}{heroImage}"
			name="og:image"
		/>
	{:else}
	{/if}
	<meta content={description} name="description" />
	<meta content={description} name="og:description" />
</svelte:head>