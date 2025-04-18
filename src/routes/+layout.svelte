<script lang="ts">
	import type { LayoutProps } from "./$types";
	import '$lib/icons/DypnoticLogo.svelte'
	import '$lib/global.css'
  import Navigation from "$lib/components/navigation.svelte";
	let { children }: LayoutProps = $props();
</script>

<svelte:head>
	<link href="/media/images/dypnotic-logo.svg" rel="icon" />
	<link rel="preconnect" href="https://fonts.bunny.net" />
</svelte:head>

<Navigation />

{@render children()}

