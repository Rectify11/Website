<script lang="ts">
  import "fluent-svelte/theme.css";
  import { Button } from "fluent-svelte";
</script>

<main>
  <div>
    <Button>Hi!</Button>
  </div>
</main>

<style>
	@import url("https://unpkg.com/fluent-svelte/theme.css");

	/* Some base styles to get things looking right. */
	:global(body) {
		background-color: var(--fds-solid-background-base);
		color: var(--fds-text-primary);
	}
</style>

