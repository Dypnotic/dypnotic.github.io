<script>
	import DypnoticLogo from "$lib/icons/DypnoticLogo.svelte";
</script>

<header>
<nav class="menu">
	<a
		href="/"
		aria-label="The Dypnotic Logo. A fat cross with a short arrow on the bottom pointing up. It is an abstraction of a palm tree."
	>
		<DypnoticLogo />
	</a>
	<ul>
		<li><a href="/i">About me</a></li>
		<li><a href="/i">Design</a></li>
	</ul>
</nav>
</header>

<style>
nav {
	display: flex;
	justify-content: space-between;
}

	ul {
		padding: none;
		list-style: none;
		display: flex;
		gap: var(--distance-l);
	}
</style>
